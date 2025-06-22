overnança e Compliance** 

Governança e Compliance são aspectos tão críticos quanto a própria arquitetura técnica no Azure. São como o conjunto de **políticas, processos e ferramentas** que garantem que seus recursos na nuvem estejam alinhados com os objetivos de negócios, padrões de segurança e requisitos legais. Seus principais objetivos são:

- **Controle de Custos:** Evitar gastos excessivos e otimizar o uso de recursos. Ferramentas como o **Azure Cost Management + Billing** ajudam a monitorar, alocar e prever gastos.
- **Segurança:** Proteger seus dados e infraestrutura contra ameaças. Isso envolve a implementação de controles de acesso (RBAC), uso de firewalls, criptografia e monitoramento de segurança.
- **Consistência de Recursos:** Garantir que os recursos sejam provisionados e configurados de maneira padronizada. O **Azure Policy** é fundamental aqui, permitindo definir regras que os recursos devem seguir (ex: apenas VMs de um certo tamanho, tagging obrigatório, regiões permitidas).
- **Organização e Gerenciamento:** Estruturar o ambiente de forma lógica para facilitar o gerenciamento. Isso é feito através de **Resource Groups**, **Subscriptions** e **Management Groups**.
- **Automação:** Automatizar a aplicação de políticas e configurações para reduzir erros humanos e aumentar a eficiência.

**Ferramentas Chave para Governança:**

- **[Azure Policy](<AzurePolicy.md>):** Cria, atribui e gerencia políticas que impõem regras e efeitos sobre seus recursos.

- **[Azure Blueprints](<AzureBlueprints.md>):** Permite implantar e atualizar ambientes inteiros de forma repetível, padronizando a implantação de um conjunto de recursos, políticas e atribuições de função.
- **Azure Resource Groups, Subscriptions e Management Groups:** Oferecem uma hierarquia lógica para organizar e gerenciar recursos e políticas em diferentes níveis.
- **Azure Cost Management + Billing:** Para monitoramento e otimização de custos.
- **Azure Monitor e Azure Security Center (Microsoft Defender for Cloud):** Para monitoramento de performance e segurança.