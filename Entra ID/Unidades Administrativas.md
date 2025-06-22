### **Unidades Administrativas**

Uma Unidade Administrativa é um **contêiner lógico para usuários e grupos**. Ela permite que você defina um escopo administrativo limitado, dentro do qual administradores específicos podem gerenciar apenas os objetos designados. Isso significa que você pode:

- **Delegar o gerenciamento por localidade:** Se você tem filiais em diferentes cidades, pode criar AUs para cada filial e designar administradores locais para gerenciar usuários e grupos apenas daquela localidade.
- **Delegar o gerenciamento por departamento:** Departamentos como RH, Vendas ou TI podem ter seus próprios administradores que gerenciam apenas os usuários e grupos de seu respectivo departamento.
- **Restringir privilégios:** Em vez de dar a um administrador uma função de "Administrador de Usuário" global (que permitiria gerenciar todos os usuários na organização), você pode atribuir essa função, mas escopada a uma Unidade Administrativa específica.


#### Como Funcionam as Unidades Administrativas?

1. **Criação da AU:** Você cria uma Unidade Administrativa no Microsoft Entra ID.
2. **Adição de Membros:** Você adiciona **usuários e/ou grupos** a essa Unidade Administrativa. É importante notar que um usuário ou grupo pode ser membro de várias AUs.
3. **Atribuição de Administradores:** Você então atribui **funções de administrador do Entra ID** (como "Administrador de Usuário", "Redefinidor de Senha", "Leitor de Diretório") a usuários ou grupos, mas especifica que essa função se aplica **apenas dentro do escopo** daquela Unidade Administrativa.

#### Vantagens Chave:

- **Princípio do Menor Privilégio:** As AUs reforçam o princípio do menor privilégio, garantindo que os administradores só tenham as permissões necessárias para suas responsabilidades específicas.
- **Redução da Superfície de Ataque:** Limitar o escopo das permissões de administração reduz o risco de um comprometimento de conta de administrador afetar toda a organização.
- **Gerenciamento Descentralizado:** Facilita o gerenciamento de grandes diretórios, permitindo que as equipes locais ou departamentais cuidem de suas próprias identidades sem a necessidade de intervenção da TI central para cada pequena tarefa.
- **Conformidade e Auditoria:** Ajuda a atender requisitos de conformidade ao fornecer um controle mais granular sobre quem pode gerenciar quais identidades.

- Podemos adicionar Users, Computers e Groups.
- As funções devem ser definidas dentro do escopo da AU.
- No portal do Azure somente usuários Administrador Global ou Administrador de função com privilégios podem gerenciar AUs.
- Ferramentas de gerenciamento: Portal do Azure, cmdlets e scripts do PowerShell ou Microsoft Graph.
- Admnistrative Units Restritas, só podem ser gerenciadas por usuários Administrador de função com privilégios especificos.
- Usuários Global Admins não podem gerenciar a menos que inclua as devidas permissões ao próprio usuário. 

#### Links de referência:
[Como restringir o acesso ao centro de administração do Microsoft Entra – Blog do Chesley](https://chesley.com.br/2024/02/23/como-restringir-o-acesso-ao-centro-de-administracao-do-microsoft-entra/)
[Isolamento de recursos seguro em um único locatário no Microsoft Entra ID - Microsoft Entra | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/architecture/secure-single-tenant)
