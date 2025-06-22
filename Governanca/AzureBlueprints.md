### Azure Blueprints: Orquestrando Implantações Repetíveis e Conformidade

O **Azure Blueprints** é como um **pacote completo de automação e conformidade para a implantação de ambientes**. Ele permite que você defina um conjunto repetível de recursos, atribuições de função, políticas e outros artefatos que podem ser implantados em uma Subscription Azure de forma consistente.

**Principais funcionalidades e usos:**

- **Implantações Padronizadas:** Crie "projetos" (blueprints) que contêm tudo o que é necessário para construir um ambiente específico (por exemplo, um ambiente de "desenvolvimento seguro" ou um ambiente de "produção conforme LGPD"). Isso inclui:
    - **Resource Groups:** Para organizar seus recursos.
    - **Azure Resource Manager (ARM) templates:** Para definir a infraestrutura (VMs, redes, bancos de dados, etc.).
    - **Azure Policy assignments:** Atribua políticas para garantir a conformidade desde o momento da implantação.
    - **Role Assignments (RBAC):** Defina quem tem acesso a quais recursos.
- **Conformidade de Linha de Base:** Garanta que, ao implantar um novo ambiente, ele já nasça em conformidade com as políticas e controles de acesso definidos. O Blueprint "trava" alguns desses elementos, dificultando sua remoção acidental ou intencional.
- **Orquestração de Implantação:** Os Blueprints oferecem uma forma orquestrada de implantar esses artefatos, rastreando o progresso da implantação e garantindo que o ambiente seja configurado como planejado.
- **Gerenciamento do Ciclo de Vida:** Permite versionar seus projetos e atualizar ambientes já implantados com novas versões do blueprint, mantendo a conformidade ao longo do tempo.

#### Links de referências:

[Documentação do Azure Blueprint | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/blueprints/)
[Início Rápido: Criar um blueprint no portal - Azure Blueprints | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/blueprints/create-blueprint-portal)
[Tutorial: Amostra do blueprint para o novo ambiente - Azure Blueprints | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/blueprints/tutorials/create-from-sample)
[Entender ciclo de vida de um blueprint - Azure Blueprints | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/blueprints/concepts/lifecycle)
[Compreender o bloqueio de recursos - Azure Blueprints | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/blueprints/concepts/resource-locking)