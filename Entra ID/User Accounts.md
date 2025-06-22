Todos os usuários da organização precisam ter uma conta para utilizar os serviços disponíveis.
- A conta é utilizada para autenticação e autorização.
- Cada conta de usuário tem propriedades adicionais.

É possível sincronizar os usuários do AD DS (on-Premises) com o MS Entra ID. A replicação é sempre em um único sentido do AD DS on-Premises para o Entra ID. Não é possível replicar os usuários do Entra ID para o AD DS.

* Deve ser Global Admin ou Administrado de usuários para gerenciar usuários.
* O informações adicionais (Foto, trabalho, departamento, info de contato, etc) são opcionais.
* Usuários excluídos podem ser restaurados por 30 dias.
* Informações de logon e log de auditoria estão disponíveis.
* é possível convidar usuários de outros domínios ou serviços (google, facebook, etc) para participar da organização.
* Suporta criar, excluir e listar usuários em massa.


>✏️ Questão de prova AZ-104
>***Qual a diferença entre a Role Owner e Contributor?***
>O Owner é o proprietário do recurso e pode executar todas as operações possíveis. Já o Contributor pode executar todas as operações com exceção de adicionar privilégios.

Tipos de contas de usuários:

- *Identidade de nuvem:*
- *Identidade sincronizada:*
- *Usuário Convidado:*

Formas possíveis de criar usuário:

- Através do portal do Entra ID, Azure ou MS 35.
- utilizando arquivos .CSV para criar usuários em massa.
- PowerShell
- MS Graph.


-----------
## **Links de referência:**

[Como as identidades gerenciadas para recursos do Azure funcionam com máquinas virtuais do Azure - Managed identities for Azure resources | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/managed-identities-azure-resources/how-managed-identities-work-vm)