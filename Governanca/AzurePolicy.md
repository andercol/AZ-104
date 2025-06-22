#### Azure Policy: Impondo Padrões e Conformidade

Pense no **Azure Policy** como um sistema de **auditoria e aplicação de regras** em seu ambiente Azure. Ele permite que você defina e imponha requisitos para os recursos, garantindo que eles permaneçam em conformidade com os padrões da sua organização e regulamentações. 
Também podemos dizer que é semelhante as GPOs do Active Directory, mas não chega ao nivel do S.O (é como se fosse uma GPO do Azure) recurso que permite que seja aplicado configuração em massa.

**Principais funcionalidades e usos:**

- **Definição de Regras:** O Azure Policy permite criar "definições de política" que especificam quais condições os recursos devem atender (por exemplo, "todas as máquinas virtuais devem ter criptografia de disco habilitada", "apenas tipos de máquinas virtuais aprovados podem ser implantados", "recursos só podem ser criados em regiões específicas").
- **Auditoria e Correção:** As políticas podem auditar recursos existentes para identificar não conformidade ou aplicar automaticamente correções. Por exemplo, uma política pode detectar um recurso sem uma tag específica e adicioná-la automaticamente.
- **Prevenção de Não Conformidade:** As políticas podem impedir a criação ou atualização de recursos que não atendem aos seus requisitos, garantindo que o ambiente permaneça limpo desde o início.
- **Conformidade Regulamentar:** Utilize políticas para ajudar a cumprir regulamentações como LGPD, GDPR, HIPAA, exigindo configurações de segurança específicas ou restrições de localização de dados.
- **Gerenciamento de Custos:** Impeça a implantação de tipos de recursos caros ou defina limites para o uso de determinados serviços.

**Pode ser aplicado a:**
- Management Group
- Subscription
- Resource Group

-------
Politica Default - padrão da Microsoft.

Definição:

- 2x padrões:
	- **Policy definition:** é uma configuração exclusiva para um determinado escopo que estou aplicando. (Subscription, Management Group, Resource Group)
	- **Initiative definition:** é conjunto de múltiplas politicas, são composto de várias  politicas que tem o objetivo de atender um padrão de compliance. 
		- Ex.: implementar padrão ISO 27001 no ambiente. (ira entregar um conjunto de 459 politicas que a MS colocou que irão ajudar para atender esse padrão )
	- *Após aplicar as politicas o Azure ira varrer a estrutura e apresentar os itens que estão em compliance e os que não estão em: Policy > Compliance.*

Podemos definir o processo de aplicação de Politicas em três tempos:
1. Aplicar as politicas.
2. Validar o compliance para entender o que está ok e o que não está.
3. Ajustar os itens que não estão compliance.

Considerações ao usar o Azure Policy

- Considere recursos implantáveis: especifique tipos de recursos permitidos, SKUs de VM etc.
- Considere restrições de localização: restrinja os locais que os usuários podem implantar recursos.
- Considere a imposição de regras: impor regras de conformidade e opções de configuração, tags necessárias em recursos e definir os valores permitidos.
- Considere auditorias de inventário: use o Azure Policy com o serviço de backup em suas VMs e execute auditorias de inventário.


> *é possível aplicar politicas no ambiente local utilizando o Azure Arc.*

> 💡Questão de prova AZ-104
> **Em qual escopo eu posso aplicar uma policy?** - R: Subscription, Management Group, Resource Group
> A TAG não é um recurso herdável, se aplicar uma tag em um resource group não ira replicar para os recursos internos. Mas podemos forçar a herança via policy.


##### Casos de uso

*Tipos de recursos permitidos* - Especificar os tipos de recursos que sua organização pode implantar
*As SKUs de máquina virtual permitida* - Especificar um conjunto de SKUs de máquina virtual que sua organização pode implantar.
*Locais permitidos* - Restringir os locais que sua organização pode especificar ao implantar recursos.
*Exigir a marca e seu valor* - Impõe uma marga necessária e seu valor.
*O Backup do Azure deve ser habilitado para máquinas virtuais* - Audite se o serviço de Backup está habilitado para todas as máquinas virtuais.


#### Scopo (Tag / RBAC / Policy / Lock):

|                       | Tag | RBAC | Policy | Lock |
| --------------------- | --- | ---- | ------ | ---- |
| Root Management Group | N/A | N/A  | N/A    | N/A  |
| Management Group      | N/A | Sim  | Sim    | N/A  |
| Subscription          | Sim | Sim  | Sim    | Sim  |
| Resource Group        | Sim | Sim  | Sim    | Sim  |
| Resource              | Sim | Sim  | N/a    | Sim  |


---------

#### Links de referências:

[Introdução ao Azure Policy - Training | Microsoft Learn](https://learn.microsoft.com/pt-br/training/modules/intro-to-azure-policy/)
[Documentação do Azure Policy | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/policy/)
[Início Rápido: Criar atribuição de política usando o portal do Azure - Azure Policy | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/policy/assign-policy-portal)
[Tutorial: Criar políticas para impor conformidade - Azure Policy | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/policy/tutorials/create-and-manage)
[Tutorial: Criar uma definição de política personalizada - Azure Policy | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/policy/tutorials/create-custom-policy-definition)
[Detalhes das noções básicos da estrutura de definição do Azure Policy - Azure Policy | Microsoft Learn](https://learn.microsoft.com/pt-br/azure/governance/policy/concepts/definition-structure)
