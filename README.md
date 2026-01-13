<div align="Center"> 
<br>

<h3>

░█████╗░███████╗██╗░░░██╗██████╗░███████╗
██╔══██╗╚════██║██║░░░██║██╔══██╗██╔════╝
███████║░░███╔═╝██║░░░██║██████╔╝█████╗░░
██╔══██║██╔══╝░░██║░░░██║██╔══██╗██╔══╝░░
██║░░██║███████╗╚██████╔╝██║░░██║███████╗
╚═╝░░╚═╝╚══════╝░╚═════╝░╚═╝░░╚═╝╚══════╝
</h4>
</div>

----

<details>
  <summary><b> 1. Tópicos</b></summary>
<div align="Left">  
<br>  

A1.1 - Azure Regions | Regiões do Azure 
 > - Área geográfica que contém um ou mais datacenters próximos entre si, conectados por uma rede de baixa latência;
 > - As regiões importam, porque afetam a latência, conformidade legal / residência de dados, e disponibilidade de dados.
 >
 > - Cada região do Azure fica emparelhada com outra região dentro da mesma geografia: Region Pair / Par de Região;
 > - Características dos Pares de Região:
 >   - Distância mínima de 300 miles / 480 kms;
 >   - Atualizações planejadas são feitas uma região por vez;
 >   - Replicação automática de dados em alguns serviços.
 > - Benefícios dos Pares de Região:
 >   - Recuperação de desastres;
 >   - Alta disponibilidade;
 >   - Continuidade de negócios.
 >  
 > - Regiões Soberanas / Sovereign Regions são instâncias isoladas do Azure;
 > - Atendem requisitos legais e governamentais específicos.
 > - Exemplos:
 >   - Azure Government (EUA);
 >   - EUA China - Operado pela 21Vianet;
 >   - Azure Germany
 > - Características:
 >   - Isoladas do Azure Público;
 >   - Atendem leis locais e requisitos de compliance;
 >   - Acesso e autenticação diferenciados.                     

A1.2 - Availability Zones | Zonas de Disponibilidade 
 > - Localização física separada, dentro de uma região do Azure;
 > - Cada zona possui:
 >   - Datacenters independentes;
 >   - Energia, refrigeração e rede próprias;
 >   - Conectividade de alta velocidade entre zonas.
 > - Normalmente, uma região possui 3 zonas de disponibilidade.
 > - Elas protegem contra falhas de datacenter, aumentam a alta disponibilidade - sendo ideais para aplicações críticas.
 >
       
A1.3 - Azure Datacenters 
 > - Instalações físicas onde os servidores são hospedados, dados armazenados, e serviços executados;
 > - Operam com redundância de energia, refrigeração e rede;
 > - O acesso pelos clientes é sempre lógico: Portal, CLI, APIs.  
 > - Região -> Zona de Disponibilidade -> Datacenters:
 >   - Região
 >   - |_ Zona de Disponibilidade 1
 >   -    |_ Datacenter(s)
 >   - |_ Zona de Disponibilidade 2
 >   -    |_ Datacenter(s)
 >   - |_ Zona de Disponibilidade 3
 >   -    |_ Datacenter(s)

A1.4 - Azure Resources 
 > - Recurso é qualquer serviço individual criado no Azure.
 > - Exemplos:
 >   - VMs;
 >   - Bancos de Dados;
 >   - Redes Virtuais.
 > - É a menor unidade gerenciável no Azure.      

A1.5 - Resource Groups 
 > - Contêiner lógico que organiza recursos relacionados.
 > - Características:
 >   - Um recurso pertence a APENAS UM resource group;
 >   - Recursos do mesmo grupo podem estar em regiões diferentes;
 >   - Facilita gerenciamento, controle, exclusão, em conjunto - por estar com recursos agrupados.
 > - Exemplo: Um resource group para uma aplicação web, que contém VM, banco de dados e rede.

A1.6 - Subscriptions  
 > - Limite administrativo e de faturamento no Azure.
 > - Funções principais:
 >   - Controla Custos - Cada assinatura tem sua própria fatura;
 >   - Define Limites de Uso (quotas);
 >   - Aplica permissões (RBAC).
 > - Exemplos: Uma assinatura para ambiente de Desenvolvimento, e outra assinatura para Produção.

A1.7 - Management Groups
 > - Permitem gerenciar várias assinaturas, de forma centralizada.
 > - Funções:
 >   - Aplicar políticas, roles e compliance em várias assinaturas ao mesmo tempo;
 >   - Organizar grandes ambientes corporativos.
 > - Hierarquia:
 >   - |_ Management Groups: Governança Global de Custos e Acessos;
 >   - |_ Subscriptions: Controle de Custos e Acesso;
 >   - |_ Resource Groups: Organização Lógica de Serviços;    
 >   - V_ Resources: Serviços Individuais   

</div> 
</details>

----
