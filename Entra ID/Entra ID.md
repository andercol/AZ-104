### Microsoft Entra ID
O Micrsoft Entra ID é serviço de diretório semelhante ao Windows Active director,  um conjunto recursos de gerenciamento baseado em nuvem que fornece o gerenciamento de usuários, aplicativos, autenticação, autorização, dispositivos e identidade híbrida. Permite a administrar e gerenciar com segurança o acesso aos serviços e recursos do Azure.

- SAML
- Oauth
- OpenID
- WS-Federation

Conceitos:

| Conceito           | Descrição                                                                                                                                                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Identity          | Um objeto que pode ser autenticado                                                                                                                                                                                                           |
| Account           | Uma identidade que possui dados associados.                                                                                                                                                                                                  |
| Azure AD Account  | uma identidade criada pelo Azure Entra ID ou outro serviço de nuvem da MS                                                                                                                                                                    |
| Azure tenant | Uma instânjcia dedicada e confiável do Entra ID, criada automaticamente quando sua organização se inscreve para uma assinatura do serviço de nuvem da MS - Semelhante a uma arvore de domínio do AD, porem não existem subdominios no Azure. |
| Azure Entra ID    | Cada tenant do Azure tem um diretório dedicado e confiável do Azure Entra ID.                                                                                                                                                                |
| User Subscription | Assinatura do Serviço do Azure. Usado para pagar pelos serviços em nuvem do Azure.                                                                                                                                                           |
|                   |                                                                                                                                                                                                                                              |

**AD DS vs Microsoft Entra ID**
- Entra ID é principalmente uma solução de identidade projetada para comunicações HTTP e HTTPS
- Utiliza API REST sobre HTTP e HTTPS em vez do LDAP
- Utiliza protocolos HTTP e HTTPS, como SAML, WS-Fedreation e OpenID Connect para autenticação (e OAuth para autorização) em vez do Kerberos
- Inclui serviços de federação e muitos serviços de terceiros (Como o Facebook)
- Os usuários e grupos são criados em uma extrutura plana e não existem Unidades Organizacionais (OUs) nem Objetos de Diretiva de Grupos (GPOs)

**Azure AD Join** - processo de adicionar uma maquina no Azure.

* [MS Entra ID - User Accounts](<MS Entra ID - User Accounts.md>)
* [MS Entra ID - Groups]
* [MS Entra ID - Unidades Administrativas (UAs)]
* [Governance - Subscriptions]
* [MS Entra ID - Licenciamento]
* [MS Entra ID - Segurança]
* [MS Entra ID - Self-Service Password Reset]
* 

#### Identidades no Entra ID

Uma identidade no Entra ID é um objeto autenticado e autorizado para acesso a um recurso. 
As identidades podem ser humanas ou não humanas:
	Humanas são conhecidas como *Identidades*
	Não humanas são conhecidas como *Identidades de caga de trabalho*.
		- Objetos de aplicativos
		- Entidades de serviço
		- Identidades gerenciadas e dispositivos
	A identidade de carga de trabalho autentica e acessa outros serviços e recursos.


>💡Info 
>[Identidades de carga de trabalho - Microsoft Learn](https://learn.microsoft.com/pt-br/entra/workload-id/workload-identities-overview) 

O Tenant do Microsoft Entra é um limite de segurança de identidade controlado por administradores.
A administração de assinaturas, grupos de gerenciamento e grupos de recursos podem ser delegados para controle administrativo de recursos do Azure, através de configurações de políticas e definições em todo o locatário.

O MS 365 tem vários sistemas de controle de acesso baseado em função que foram desenvolvidos independentemente ao longo do tempo, cada um com o próprio portal de serviço. 
Por conveniência a Microsoft incluiu algumas funções administrativas no Entra ID para cada serviço do MS 365 como: Administrador do Exchange, Administrador do Teams, Administrador do Sharepoint, etc. Essas funções possui outras [[#funções equivalentes]] nos seus respectivos portais. 
Ex.: *Administrador do Exchange* (no Entra ID) é equivalente ao *grupo de funções de Gerenciamento da Organização* no Exchange.
Dentre os diferentes serviços do Microsoft 365, os serviços abaixo têm os próprios sistemas de controle de acesso baseado em função?

- ID do Microsoft Entra
- Microsoft Exchange
- Microsoft Intune
- Microsoft Defender for Cloud Apps
- Portal do Microsoft 365 Defender
- Portal de conformidade
- Gerenciamento de Custos + cobrança

Os serviços abaixo não têm sistemas de controle de acesso baseado em função próprio e utilizam as funções do Microsoft Entra ID para acesso administrativo.
- Teams
- SharePoint
- Área de Trabalho Gerenciada

O **Azure** tem seu próprio sistema de controle de acesso baseado em funções para os recursos do Azure (RBAC).

> No portal do Azure é possível verificar a lista de funções do Microsoft Entra na página Funções e Administradores "Roles and administrators"

Em um nível alto, as funções do Azure controlam permissões para gerenciar recursos do Azure, enquanto as funções do Microsoft Entra controlam permissões para gerenciar recursos do Microsoft Entra. A tabela a seguir compara algumas das diferenças.

|Funções do Azure|Funções do Microsoft Entra|
|---|---|
|Gerenciar o acesso aos recursos do Azure|Gerenciar o acesso aos recursos do Microsoft Entra|
|Dá suporte a funções personalizadas|Dá suporte a funções personalizadas|
|O escopo pode ser especificado em vários níveis (grupo de gerenciamento, assinatura, grupo de recursos e recursos)|O [escopo](https://learn.microsoft.com/pt-br/azure/active-directory/roles/custom-overview#scope) pode ser especificado no nível do locatário (em toda a organização), na unidade administrativa ou em um objeto individual (por exemplo, um aplicativo específico)|
|As informações de função podem ser acessadas no portal do Azure, na CLI do Azure, no Azure PowerShell, nos modelos do Azure Resource Manager, na API REST|As informações de função podem ser acessadas no portal do Azure, Centro de administração do Microsoft Entra, Centro de administração do Microsoft 365, Microsoft Graph, Microsoft Graph PowerShell|

>✏️**Conta Global de inscrição do Azure**
>  A conta utilizada para se inscrever nos serviços do Azure recebe as funções:
>- Administrador da Conta
>- Administrador de Serviços (equivalente a função Proprietário).

#### [Governance - Subscriptions]

As assinaturas do Azure é utilizada para estabelecer um relacionamento de cobrança. Uma conta do Azure é uma identidade de usuário, uma ou mais assinaturas e um conjunto de recursos associados.
Assinaturas ajudam a organizar o acesso aos recursos do Azure e controlar como são cobrados e pagos e reportar o uso.
Pode se configurar varias assinaturas, com diferentes formas de cobrança e pagamento. Podendo criar assinaturas e planos diferentes por escritório, departamento, projeto, centro de custo, etc.

----------------

#### Microsoft Entra Domain Services
Uma alternativa ao Active Directory Domain Services na nuvem, permitindo que tenha funcionalidades semelhantes ao ADDS implantado localmente e que utilizam LDAP, NTLM ou protocolos Kerbero.
**Benefícios:**
- Não precisa ser gerenciar, atualizar e monitorar controladores de domínio.
- não precisa implantar e gerenciar a replicação do Active Directory.
- não é necessário ter administradores de domínio ou grupos de administradores de empresa para domínios que o MS Entra ID gerencia.

**Limitações:**
- Suporte apenas para objeto do Active Directory do computador base
- estender o esquema para o domínio do Entra Domain Services
- Estrutura de OUs é simples e não há suporte para OUs aninhadas no momento.
- GPO interno existente para contas de computador e susuário.
- Não é possível direcionar OUs com GPOs internos e não pode usar filtros de WMI, nem filtragem de grupo de segurança.

-----------
## **Links de referência:**

- [Introdução à administração delegada e ambientes isolados - Microsoft Entra | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/architecture/secure-introduction)
- [Funções do Azure, funções do Microsoft Entra e funções clássicas de administrador de assinatura | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/role-based-access-control/rbac-and-directory-admin-roles)
- [Entender os conceitos de funções do Microsoft Entra - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/role-based-access-control/concept-understand-roles)
- [Elevar o acesso para gerenciar todas as assinaturas e grupos de gerenciamento do Azure | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/role-based-access-control/elevate-access-global-admin?tabs=azure-portal)
- [Zero trust configuration for multitenant defense organizations - Cloud Adoption Framework | Microsoft Learn](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/defense/identity/multi-tenant/zero-trust-configuration)
- [Funções nos serviços da Microsoft - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/role-based-access-control/m365-workload-docs)
- [Funções internas do Microsoft Entra - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/role-based-access-control/permissions-reference)
- [Introdução aos inquilinos do Microsoft Entra - M365 Education | Microsoft Learn](https://learn.microsoft.com/pt-br/microsoft-365/education/deploy/intro-azure-active-directory)