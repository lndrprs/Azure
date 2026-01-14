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
  <summary><b> 1. Tópicos Fundamentais</b></summary>
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

A1.8 - Compute Types: Virtual Machines, Containers e Functions
 > - VMs
 >   - Simulam um servidor completo: SO + Aplicações;
 >   - Gerenciamento do Sistema Operacional;
 >   - Maior controle, maior responsabilidade.
 >     - Usabilidades:
 >       - Aplicações Legadas;
 >       - Softwares que exigem controle total do SO.
 >
 > - Containers
 >   - Executam aplicações isoladas, compartilhando o Kernel do SO;
 >   - Mais leves que VMs;
 >   - Inicializam rapidamente.
 >     - Serviços Azure:
 >       - Azure Container Instances (ACI);
 >       - Azure Kubernetes Service (AKS).
 >     - Usabilidade:
 >       - Microsserviços;
 >       - Aplicações Modernas e Escaláveis.
 >      
 > - Functions
 >   - Executam código sob demanda, acionado por eventos;
 >   - Não há gerenciamento de servidores;
 >   - Cobrança baseada em execuções.
 >     - Usabilidade:
 >       - Processamento sob demanda;
 >       - APIs simples;
 >       - Automação e Eventos.                       

A1.9 - Virtual Machine Options 
 > - Azure Virtual Machines
 >   - VMs individuais;
 >   - Controle total do S.O;
 >   - Suporta Windows e Linux.
 > 
 > - Virtual Machine Scale Sets (VMSS)
 >   - Conjunto de VMs idênticas;
 >   - Escala automática (horizontal);
 >   - Ideal para workloads variáveis.
 >     - Exemplo: Aplicações web com picos de acesso.        
 >
 > - Availability Sets
 >   - Garantem alta disponibilidade dentro de um datacenter;
 >   - Distribuem VMs em:
 >     - Fault Domains (Falhas Físicas) - Limite de 3 por conjunto;
 >     - Update Domains (Manutenções) - Limite de 20 por conjunto.
 >
 > - Azure Virtual Desktop (AVD)
 >   - Ambiente de desktop e apps virtualizados;
 >   - Acesso remoto seguro;
 >   - Substitui infraestrutura VDI Local.
 >
 > - Resources Required for Virtual Machines
 >   - Virtual Network (VNet);
 >   - Subnet (Dentro da VNet);
 >   - Network Security Group - Sendo associada na Subnet ou NIC;
 >   - Network Interface (NIC) - Recebe IP Privado Automaticamente;
 >   - IP Público (Opcional);
 >   - Disco do SO;
 >   - Discos de Dados (Opcional);
 >   - Virtual Machine.
 >     - Ordem Resumida:
 >       - VNet -> Subnet -> NSG -> NIC -> Discos -> VM
 >       - Networking -> Security -> Interface -> Storage -> Compute
 >         - Não existe VM sem NIC;
 >         - Não existe NIC sem Subnet;
 >         - Não existe Subnet sem VNet;
 
A1.10 - Application Hosting Options
 > - Web Apps (Azure App Service)
 >   - Plataforma gerenciada para apps web;
 >   - Suporte a .Net, Java, Node.js, Python;
 >   - Alta disponibilidade embutida.
 >     - Ideal para: Sites e APIs.
 >
 > - Containers
 >   - Aplicações empacotadas;
 >   - Portabilidade entre ambientes;
 >   - Executados via ACI ou AKS;
 >     - Ideal para Microsserviços e aplicações distribuídas.
 >
 > - Obs.: VMs podem ser uma opção para aplicações legadas ou personalizadas.

A1.11 - Virtual Networking
 > - Azure Virtual Network (VNet)
 >   - Rede privada no Azure;
 >   - Permite comunicação entre recursos.
 >
 > - Subnets
 >   - Segmentam a VNet;
 >   - Ajudam na organização e segurança.
 >
 > - VNet Peering
 >   - Conecta duas VNets;
 >   - Comunicação Privada e de baixa latência;
 >   - Pode ser entre regiões.
 >
 > - Azure DNS
 >   - Serviço de Resolução de Nomes;
 >   - Hospeda Zonas DNS públicas ou privadas.
 >
 > - Azure VPN Gateway
 >   - Conexão Segura Criptografada;
 >   - Conecta a Azure a Ambiente On-Premises, e outras VNets.
 >
 > - Express Route
 >   - Conexão privada dedicada com Azure;
 >   - Não passa pela internet pública;
 >   - Mais rápida e confiável que VPN.       

A1.12 - Public Endpoint vs Private Endpoint
 > - Public Endpoint
 >   - Acessível pela internet pública;
 >   - Usa IP público.
 >     - Exemplo: Site público. 
 >
 > - Private Endpoint
 >   - Usa IP privado denrtro da VNet;
 >   - Acesso restrito à rede privada;
 >   - Mais seguro.
 >     - Exemplo: Banco de dados acessado internamente.
    
A1.13 - Azure Storage Services 
 > - Azure Storage possui quatro serviços principais:
 >   - Blob Storage
 >     - Armazena objetos - arquivos, imagens, vídeos, backups;
 >     - Ideal para dados não estruturados.
 >     - Muito usado para:
 >       - Backups;
 >       - Data Lakes;
 >       - Conteúdos Estáticos de Sites.
 >
 >   - File Storage | Azure Files
 >     - Compartilhamentos de Arquivos na Nuvem;
 >     - Acesso via SMB ou NFS;
 >     - Pode substituir servidores de arquivos locais;
 >     - Integração com Azure File Sync.
 >
 >   - Queue Storage
 >     - Armazena mensagens para comunicação assíncrona entre aplicações;
 >     - Usado para desacoplamento de Sistemas.
 >
 >   - Table Storage
 >     - Armazenamento NoSQL (Chave - Valor);
 >     - Ideal para grandes volumes de dados estruturados, mas não relacionais.
                
 A1.14 - Storage Tiers | Camadas de Armazenamento 
 > - As camadas controlam Custo x Desempenho:
 >   - Hot
 >     - Acesso Frequente;
 >     - Maior custo de armazenamento;
 >     - Menor custo de acesso.
 >
 >   - Cool
 >     - Acesso menos frequentes;
 >     - Armazenamento mais barato;
 >     - Custo maior para leitura / gravação.
 >
 >   - Archive
 >     - Acesso raro;
 >     - Muito barato para armazenar;
 >     - Recuperação lenta (horas);
 >     -  Ideal para backups e retenção de longo prazo.

A1.15 - Redundancy Options 
 > - Definição de como os dados serão replicados:
 >   - LRS - Locally Redundant Storage
 >     - 3 cópias no mesmo datacenter;
 >     - Mais barato;
 >     - Protege contra falhas locais.
 >
 >   - ZRS - Zone-Redundant Storage
 >     - Replicação entre zonas de disponibilidade;
 >     - Alta disponibilidade dentro da região.
 >
 >   - GRS - Geo-Redundant Storage
 >     - Replica dados para outra região;
 >     - Protege contra falhas regionais.
 >
 >   - GZRS - Geo-Zone-Redundant Storage
 >     - Combina ZRS e GRS

A1.16 - Storage Account Options and Storage Types
 > - Tipos de Storage Account:
 >   - General Purpose v2 (GPv2): Padrão recomendado;
 >   - Blob Storage Account: Otimizada apenas para Blobs;
 >   - FileStorage: Otimizada para Azure Files (Premium).
 >
 > - Tipos de Armazenamento:
 >   - Standard: HDD, mais barato;
 >   - Premium: SSD, alto desempenho e baixa latência.

A1.17 - Options for Moving Files
 > - AzCopy
 >   - Ferramenta de linha de comando;
 >   - Transferência rápida de dados para / de Blob e File Storage;
 >   - Ideal para grandes volumes.
 >
 > - Azure Storage Explorer
 >   - Interface gráfica;
 >   - Facilita upload, download e gerenciamento;
 >   - Uso manual e visual.
 >
 > - Azure File Sync
 >   - Sincroniza arquivos locais com Azure Files;
 >   - Mantém cache local;
 >   - Ideal para Ambientes Híbridos.

A1.18 - Migration Options
 > - Azure Migrate
 >   - Avaliação e Migração de:
 >     - Servidores;
 >     - Máquinas Virtuais;
 >     - Bancos de Dados.
 >   - Ajuda a planejar custos e compatibilidade.
 >
 > - Azure Data Box
 >   - Dispositivo físico da Microsoft;
 >   - Usado quando volume de dados é gigante, e internet lenta / limitada;
 >   - Copia os dados localmente, e envia o dispositivo de volta à Microsoft.           
 
</div> 
</details>

----
