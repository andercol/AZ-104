### **Subscription (Assinatura)** 

É o ponto de partida fundamental para qualquer coisa que você faça no Microsoft Azure. Pense nela como uma **conta de faturamento e um limite administrativo** para seus recursos de nuvem.

Uma **Assinaturas do Azure** fornece a você acesso autenticado e autorizado às contas do Azure. (uma unidade lógica)

- **Limite de cobrança:** gerar faturas e relatórios de cobrança separados para cada assinatura.
- **Limite de controle de acesso:** gerenciar e controlar o acesso aos recursos que os usuários provisionam com assinaturas específicas.
- Geralmente é estruturado por estrutura organizacional. (exemplo: Departamento > assinaturas: Desenvolvimento, Qualidade, Produção)
- Separação de custos
- Governança e segurança do ambiente


![Subscription](..\images\AssinaturasDoAzure.png)

Uma subscription do Azure é uma unidade lógica de serviços do Azure que está vinculada a uma conta do Azure.
As subscriptions ajudam a organizar o acesso aso recursos de nuvem do Azure e a controlar como o uso dos recursos é relatado, cobrado e pago.

- Cada serviço do Azure pertence a uma subscription.
- Cada subsctiption pode ter uma configuração de cobrança e pagamento diferente.
- Várias subscription podem ser vinculadas à mesma conta do Azure.
- Mais de uma conta do Azure pode ser vinculada à mesma subscription.
- A cobrança do Azure é realizada por subscription.

Considerações sobre o uso de subscriptions:

- Considere os tipos de contas do Azure necessárias: Conta o MS Entra, Diretório confiável do Entra ID, conta corporativa ou de estudante.
- Considere várias subscriptons: configure diferentes assinaturas e opções de pagamento de acordo com os departamentos, projetos, escritórios regionais, etc.
- Considere uma subscripton dedicada de serviços compartilhados: Exemplos recursos de rede, ExpressRoute, WAN, VPN, etc.
- Cada subscripton pode ser associada a um Entra ID:

![Subscription](..\images\AssinaturasDoAzure02.png)

#### Como obter uma Subscription do Azure

- Contrato Enterprise: qualquer cliente Enterprise pode adicionar o Azure ao contrato firmando um compromisso monetário antecipado com o Azure.
- Revendedor da Microsoft: compre o Azure por meio do programa Open Licensing, que fornece uma forma simples e flexível de comprar serviços de nuvem do revendedor MS.
- Parceiro da Microsoft: Encontre um parceiro da Microsoft que possa projetar e implementar sua solução de nuvem do Azure.
- Conta gratuita pessoal: qualquer usuário pode se inscrever para obter uma conta de avaliação gratuita.

#### Tipos de assinatura:

| Assinatura | Uso                                                                                                                                        |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Gratuita   | Inclui um crédito de $200 para os primeiros 30 dias, acesso limitado gratuito por 12 meses.                                                |
| Pré-paga   | Cobra mensalmente.                                                                                                                         |
| CSP        | Contrato com possíveis descontos por meio de um Provedor Parceiro Microsoft Cloud Solutions - normalmente para pequenas e médias empresas. |
| Empresa    | Um contrato, com descontos para novas licenças e Software Assurance - votado para organizações de escala empresarial.                      |
| Aluno      | Inclui $100 por 12 meses - deve verificar o acesso do aluno.                                                                               |

------------

#### Gerenciamento de Custos da Microsoft

- O gerenciamento de custos da Microsoft mostra os padrões de custo e uso da organização com análises avançadas.
- Custos baseados nos fatores e preços negociados, reservas e descontos de benefício híbrido do Azure.
- Análise preditiva também esta disponível.
- Relatórios de custos: ajudam a mostrar seus custos internos e externos de uso e encargos do MS Azure Marketplace.
- Utilize os recursos de análise de custos para explorar e analisar os custos organizacionais.
- Crie orçamentos para ajudar a planejar e cumprir a responsabilidade financeira da organização.
- Examine as recomendações para saber como otimizar e aprimorar a eficiência identificando recursos ociosos e subutilizados.

----------

#### Aplicar a marcação de recursos (Tags)

- um recurso ou grupo de recursos pode ter, no máximo, 50 pares nome/valor de tags.
- cada tag tem um nome e um valor.
- o nome da marca permanece constante para todos os recursos que têm a tag aplicada.
- o valor da tag pode ser selecionado em um conjunto defino de valores ou ser exclusivo para uma instância de recurso especifica.

## Links de referência:

[regiões emparelhadas | Microsoft Azure](https://learn.microsoft.com/pt-br/azure/reliability/cross-region-replication-azure#azure-cross-region-replication-pairings-for-all-geographies)
[Produto do Azure por Região | Microsoft Azure](https://azure.microsoft.com/pt-br/explore/global-infrastructure/products-by-region/)
[Escolher a Região do Azure Ideal para Você | Microsoft Azure](https://azure.microsoft.com/pt-br/explore/global-infrastructure/geographies/#geographies)
