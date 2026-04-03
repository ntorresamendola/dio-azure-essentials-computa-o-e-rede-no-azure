
## Tipos de computação

### Máquinas virtuais

As máquinas virtuais do Azure são emulações de software de computadores físicos, operando dob demanda de forma escalonável na nuvem. Incluem, virtualizados, os recursos que os computadores físicos possuem: processador, memória, armazenamento e rede. 

Operam como IaaS(Infrastructure as a Service). Cabe ao usuário, você  manter a máquina virtual executando tarefas, como configurar, instalar atualizações de segurança e corrigir e instalar o software que será executado nela.

Às máquina virtuais estão relacionados recursos que podem não necessariamente ser apagados quando a máquina é excluída, como endereço de IP, disco rígido e redes virtuais.

**Conjuntos de dimensionamento de VMs** oferecem uma oportunidade de balanceamento de carga, automanticamente escalando horizontalmente os recursos.  (ou seja, adicionando ou removendo máquinas conforme a demanda)

**Conjuntos de disponibilidade de VM** são agrupamentos lógicos de máquinas virtuais para garantir alta disponibilidade, distribuindo-os entre múltiplos domínios de falha (hardware) e atualizações (software). Isso limita interrupções, garantindo que pelo menos uma VM permaneça operacional durante falhas ou manutenções. Não se paga pelo uso de um conjunto de disponibilidade em si, apenas para cada instância de máquina virtual criada. As latência comparadas com o uso de zonas de disponibilidade são menores, pois as VM são alocadas próximas entre si, mas as zonas de disponibilidade oferecem maior confiabilidade ao alocar as VM em diferente datacenters, e os conjuntos de disponibilidade não oferecem suporte a discos Ultra.

### Área de Trabalho Virtual do Azure

A Área de Trabalho Virtual do Azure é uma virtualização de área de trabalho e aplicativo executada na nuvem.  Suporta o Windows 11 e o Windows server. Não necessita executar outros servidores de gateway. Permite multissessão (vários usuários em uma VM), reduz custos de infraestrutura e integra-se nativamente com o Microsoft 365. O acesso à máquina pode ser feito não só via RDB mas também via browser, sendo ideal para trabalho remoto e híbrido.

### Serviços de contêineres do Azure

Os contêineres do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alterações sob demanda. 
Operam no modelo PaaS(Plataform as a Service), ou seja, não virtualizam uma máquina inteira, como as VM.

**Instâncias de Contêiner do Azure** executam um container ou pod de contêiners.

**Aplicativos de Contêiner do Azure** é uma plataforma serverless baseada em containers, com gerenciamento automático de infraestrutura e escala. Não requer gerenciamento do plano de controle Kubernetes.

**Serviço de Kubernetes do Azure(AKS)** é um serviço de Kubernetes gerenciado que pode ser usado para gerenciar e implantar aplicativos conteinerizados. Requer conhecimento de orquestração de contêiner. Reduz a complexidade e a sobrecarga operacional de gerenciar o Kubernetes passando grande parte dessa responsabilidade para o Azure. Ideal para orquestração de contêineres com arquiteturas distribuídas e grandes volumes de contêineres. 

### Azure Functions

Oferta de PaaS que dá suporte a operações serverless, sendo baseado em eventos. Suporta múltiplas linguagens de programação (C#, Python, JavaScript, Java, PowerShell) e escala de forma automática, sendo que apenas os recursos usados durante a execução são cobrados. Pode ser usado para criar APIs Web, responder a alterações no banco de dados, processar fluxos de IoT, gerenciar filas de mensagens, entre outras ações.

### Serviços de rede do Azure

A **Rede Virtual do Azure(VNet)** permite que os recursos do Azure se comuniquem um com os outros, com a Internet e com as redes locaos

É possível criar **pontos de extremidade públicos**, acessíveis de qualquer lugar na internet, e **pontos de extremidade privados**, acessíveis somente de dentro de sua rede.

A comunicação entre recursos do Azure pode ser feita por meio de **rede virtual**, **pontos de extremidade de serviço de rede virtual** e via **Emparelhamento de rede virtual*, que conectam redes virtuais entre si.

A comunicação com os recursos locais pode ser feita via **VPN** (rede virtual privada) ponto a site, estabelecida entre uma rede virtual e um único computador em sua rede, via **VPN site a site**, estabelecida entre seu dispositivo VPN local e um **gateway de VPN do Azure** implantado em uma rede virtual e via **Azure Express Route**, feita por uma conexão privada que não passa pela internet.

**DNS do Azure**: fornece hospedagem, resolução e balanceamento de carga de DNS para aplicativos usando a infraestrutura do Microsoft Azure usando a rede Anycast, oferecendo serviço para DNS privado e público. Oferece controle de acesso baseado em função e monitoramento e registro em log.


### Leituras adicionais

[Máquinas virtuais no Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/overview)

[Conjuntos de disponibildade](https://learn.microsoft.com/pt-br/azure/virtual-machines/availability-set-overview)

[Práticas recomendadas para obter alta disponibilidade com máquinas virtuais do Azure e discos gerenciados](https://learn.microsoft.com/pt-br/azure/virtual-machines/disks-high-availability)

[O que é a Área de Trabalho Virtual do Azure?
](https://learn.microsoft.com/pt-br/azure/virtual-desktop/overview)

[Documentação dos serviços de contêiner
 do Azure](https://learn.microsoft.com/pt-br/azure/containers/)

[O que são as Instâncias de Contêiner do Azure?
](https://learn.microsoft.com/pt-br/azure/container-instances/container-instances-overview)

[O que é o AKS (Serviço de Kubernetes do Azure)?
](https://learn.microsoft.com/pt-br/azure/aks/what-is-aks)

[Documentação do Azure Functions
](https://learn.microsoft.com/pt-br/azure/azure-functions/)

[O que é a Rede Virtual do Azure?
](https://learn.microsoft.com/pt-br/azure/virtual-network/virtual-networks-overview)

[O que é Azure ExpressRoute?
](https://learn.microsoft.com/pt-br/azure/expressroute/expressroute-introduction?toc=/azure/virtual-network/toc.json)

[Visão geral do DNS do Azure
](https://learn.microsoft.com/pt-br/azure/dns/dns-overview)

 
