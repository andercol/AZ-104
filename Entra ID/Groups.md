### Grupos do Microsoft Entra ID: Organizando e Gerenciando Acessos

Os Grupos do Microsoft Entra ID são um recurso fundamental para simplificar o gerenciamento de permissões e acessos dentro do seu ambiente Microsoft Cloud. Eles funcionam como contêineres lógicos que reúnem usuários e até mesmo outros grupos, permitindo que você atribua permissões a um conjunto de identidades de uma só vez, em vez de gerenciar permissões individualmente para cada usuário.

- **Simplificação da Atribuição de Acessos:** Em vez de adicionar usuários um por um a cada aplicativo, recurso ou função, você pode adicionar o usuário a um grupo e, em seguida, conceder permissões a esse grupo. Isso economiza tempo e reduz a chance de erros.
- **Gerenciamento de Acesso a Aplicativos:** Os grupos do Entra ID são amplamente utilizados para controlar o acesso a aplicativos SaaS (Software as a Service) como Microsoft 365 (Teams, SharePoint, Exchange Online), bem como a aplicativos personalizados desenvolvidos na sua organização.
- **Controle de Acesso Baseado em Função (RBAC) no Azure:** Você pode usar grupos do Entra ID para atribuir **funções RBAC** a recursos do Azure (Máquinas Virtuais, Storage Accounts, Redes Virtuais, etc.). Por exemplo, um grupo de "Administradores de VM" pode receber a função de "Colaborador de Máquina Virtual", permitindo que todos os membros do grupo gerenciem suas VMs.

#### **Tipos de Grupos:**

##### *Security Groups* 
- Utilizados para gerenciar o acesso a recursos do Entra ID. Só pode ser implementado por Admins do MS Entra.
##### *Microsoft 365 Groups* 
- Utilizado para colaboração em equipe, pode ser implementado por usuários normais e Admins do MS entra.
- Oferecem recursos de colaboração, como uma caixa de correio de grupo, calendário compartilhado, site do SharePoint, e são frequentemente usados em conjunto com o Microsoft Teams.

> **Grupos do Microsoft 365** são os únicos que podem ser auto deletável.

#### **Tipos de associação:**

>Para habilitar os grupos de dinâmicos é necessário ter licença P1 ou P2.

**Assigned** - usuários adicionados manualmente

**Dynamic User** - utiliza regras de associação para adicionar membros ao grupo automaticamente. ex. usuários com a propriedade "job title =  contador" são automaticamente adicionados ao grupo Contabilidade.

**Dynamic Device** - (somente grupos de segurança) utiliza atributos do dispositivo para adicionar ou remover dispositivos em grupos de segurança.

[Licenciamento](<Licenciamento.md>)


>📝Atribuição de Licenças em Grupo
>Diferente da associação de permissões ou Roles, apenas usuários associados diretamente ao grupo recebem *licença*.
>Usuários associados a *grupos aninhados* não recebem licenças.