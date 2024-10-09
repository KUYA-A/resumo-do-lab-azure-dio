
# resumo-do-lab-azure-dio
  Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

## Resumo do Lab Construindo Arquiteturas no Azure
  Neste Lab começamos a falar acerca da arquitectura e serviços, onde começamos a detalhar como funcionam as regiões e como isso está relacionado aos serviços, a disponibilidade

### Regiões do Azure
  Azure é o serviço de nuvem com mais regiões globais, mas nem todas possuem o mesmo serviços.

  Todas as regiões possuem seus pares para manter o funcionamento de serviços em caso de desastres, ou inatividade dos serviços ou datancenters principais.

  Entre as regiões podemos destacar algumas regiões soberanas:
  
  - Azure governamental (EUA)
  - Azure China (21Vianet Operators)


### Grupo de Recursos
  Alguns recursos não são disponibilizados para algumas regiões. É possivel criar marcações em recursos, para identificar os recursos com maior facilidade no momento de pagar a factura.

  Os grupos de recursos (GR) podem ser usados para armazenar todos recursos necessarios para um projecto expecifico num unico lugar.

  Ele regista as alterações realizadas nos recursos (desde a crição, edição, eliminação e movimentação), ele tambem cria uma estrutura de relação entre os recursos.

## Resumo do Lab Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure
### VM predifinidas
  A azure permite criar maquinas com alguns recursos de forma automatica, de modo a otimizar os recursos

### Conjuntos de dimensionamento da máquina virtual
  Os conjuntos de dimensionamento da máquina virtual do Azure permitem-lhe criar e gerir um grupo de VM com balanceamento de carga. O número de instâncias de VM pode aumentar ou diminuir automaticamente em resposta à procura ou a uma agenda definida. Os conjuntos de dimensionamento fornecem elevada disponibilidade às suas aplicações e permitem-lhe gerir, configurar e atualizar de forma centralizada um grande número de VM.

  Dentro do dimensionamento, podemos encontrar os seguintes modos
  - ** Atualizar manualmente a capacidade: ** Mantenha uma quantidade fixa de instâncias.
  - ** Dimensionamento automático: ** Dimensionamento com base numa métrica da CPU, em qualquer agenda.
  - ** Sem perfil de dimensionamento: ** ligar máquinas virtuais manualmente após a implementação.

![image](https://github.com/user-attachments/assets/9f42065a-9137-457a-a687-61e0c1d038c0)


### Zona de Disponibilidade
  Azure permite criar máquina em diferentes regiões, e para algumas regiões existe algumas limitações.
  Com a redundancia de armazenamento, existe a possibilidade de réplicar o armazenamento em varias zonas de modo que o que é salvo numa região é automaticamente escrito noutros discos ou nos discos de todas as regiões selecionadas.

### Sistema Operativo
  Existe uma variedade de imagens para máquina virtual, desde servidores à hosts, do Windows ao Linux das quais podemos citar algumas:
- Windows 10 Pro, version 22H2 - x64 Gen2
- Windows 11 Pro, version 22H2 - x64 Gen2
- Windows Server 2016 Datacenter - x64 Gen2
- Windows Server 2019 Datacenter - x64 Gen2
- Windows Server 2022 Datacenter: Azure Edition - x64 Gen2
- Debian 12 "Bookworm" - x64 Gen2
- Red Hat Enterprise Linux 9.4 (LVM) - x64 Gen2
- Oracle Linux 8.9 (LVM) - x64 Gen2
- SUSE Linux Enterprise Server 15 SP5 +Patching - x64 Gen2
- Ubuntu Server 24.04 LTS - x64 Gen2
-  E outros

### Armazenamento
  Está muito relacionado com tipo de tamanho e o as configurações de disponibilidade selecionada, onde o tamanho selecionado define o número de disco que a sua maquina pode ter. quanto a disponibilidade já foi meio que descrita nos pontos acima, está muito relacionada com o tempo de inatividade do serviço.

### Rede
  Como todo e qualquer dispositvo físico é necessario que seja configurado uma rede publica ou privada para configuração do tipos de acesso ao maquina virtual com o serviço de **RDP** na porta **3389** muito comum no windows ou tambem a porta **22** para o serviço de **SSH** muito usado nos sistemas Linux.
  
### Outros Serviços
- Gestão (Ms Defender, MS Entra e identidade)
- Monitoramento (Alertas, Diagnostico e estado de funcionamento)
- Avançados (Extenções, Aplicações de VM, Desempenho (NVME), )

## Resumo do Lab Dominando o Armazenamento na Azure
### Contas de armazenamento
configuramos contas de armazenamento no Azure com foco em performance, segurança e custos. Iniciamos escolhendo o tipo de conta (Standard ou Premium), conforme a necessidade de desempenho.
- ** Standard: ** Baseado em discos rígidos (HDD) para cargas de trabalho que não exigem alta performance, como arquivos, backups e logs.
- ** Premium: ** Baseado em discos de estado sólido (SSD), ideal para alta performance em cargas de trabalho, como bancos de dados e VMs.

#### Redundância de armazenamento
  Um ponto crucial é o de selecionar o modelo de replicação de dados, como LRS ou GRS, que garantem a disponibilidade e recuperação de dados. Em seguida, ajustamos o desempenho de acesso, escolhendo entre Hot, Cool ou Archive, conforme a frequência de uso dos dados.
![image](https://github.com/user-attachments/assets/19f582d6-06d9-4228-92a9-73416f3cf690)

#### Tipos de armazenamento
Também abordamos os tipos de armazenamento (** Blob, arquivos, filas, tabelas **), cada um adequado para diferentes cenários de uso.
  - Blob do Azure: Para armazenar grandes volumes de dados não estruturados, como arquivos de texto ou binários.
  - Arquivos do Azure: Sistema de arquivos totalmente gerenciado na nuvem, com compartilhamento via SMB (para migrações de servidores ou backups).
  - Fila do Azure: Para gerenciar mensagens entre diferentes partes de uma aplicação distribuída.
  - Tabela: Para armazenamento de grandes quantidades de dados estruturados (NoSQL).


### Migração do Azure
Nesta ponto, focamos no Azure Migrate, um serviço que facilita a migração de cargas de trabalho para a nuvem. Disponibilizando seriviços para varios cenários, como a migração de servidores, bancos de dados, máquinas virtuais (VMs) e até aplicações web.
![image](https://github.com/user-attachments/assets/a5f91694-564f-4671-9c43-6ca055c29ce0)
