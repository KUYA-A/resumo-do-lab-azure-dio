
# resumo-do-lab-azure-dio
  Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

## Resumo do Lab Microsoft Azure - Localizando Serviços por Categoria
  Neste Lab pode perceber que Azure oferecer uma variada gamas de serviços para que o cliente possa criar todo o seu Datacenter de forma virtual, minimizando a necessidade
de aquirir itens de varios fornecedores como no On.Primesed.

Podemos listar algumas categorias como as seguintes:
- Computação;
- Bases de Dados;
- Híbridos & MultiCloud;
- Network;
- Web & Mobile;

### 💻 Computação
  Neste local podemos encontrar varios itens para criação de **IaaS (Infrastutura como serviço)**, permitindo ao clinete construir maquinas vituais, chaves SSH, Pontos de restauro, conjunto de disponibilidade (para criar redundancia da aplicação).

  Também podemos encontrar as **plataformas como serviços ou PaaS** como serviços aplicacionais, instancias virtuais para soluções SAP e outras. E não podemos esquecer dos **microserviços**, **computação de alto desempenho**  e **nuvem hibrida** como os Azure Arc (simplifica a gestão de ambientes complexos que abrangem clouds, datacenters e dispositivos edge).

### 💾 Base de Dados
  O nome dessa categoria é auto-explicativa, ela nos apresenta soluções para criação de novas aplicações como base de dados para servidores flexiveis PostgreSQL, Azure Cosmos DB e Hyperscala de base de dabos do Azure (para entregar uma melhor performace, adaptavel e escalavel).

  Os serviços da azure também apresentam serviços de base de dados para aplicações existentes como base de dados SQL, instacias geridas, Azure Cosmos DB para MongoDB, oracle database e outros.

### ☁️ Híbridos & MultiCloud
  Aqui são apresentados os serviços de gestão híbrida e multcloud com de facilitar a interação os serviços cloud da azure com as outras platafomras cloud e até mesmo serviços on-primised. Deste modo podemos encontrar Azure Arc, Bridges ou pontes de recuros, gestore de sites (Nova ferramente sem SLA), microsoft Entra ID, Servidores de gestão de SCVMM (Sistema de gestão para as maquinas virtuais) , Serviços de dados (como do azure Arc e SQL do Azure), Serviços de segurança como MS Sentinel e MS Defender para Cloud.
  
### 📶 Network
  Outro nome auto-explicativo, podemos encontrar serviços para Fundação de rede, Conectividade híbrida, Segurança de Rede,Balanceamento de carga, e outros.

  Resumindo, podemos encontrar tudo que é necessario para construir a nossa rede virtual, links privados realizar NAT entre as redes e a internet, criação de WAN virtuais, montar farewalls e fazer a gestão dos mesmos, monitorar, comunicar com nossa rede on-primised ou outra cloud e todo tipo de serviço de rede.


### 🌐 Web & Mobile
  Aqui onde podemos encontrar serviços para gestão de API (como ligações e serviços de gestão de API), Infraestrutura da aplicações, Gestão de aplicações, serviços de multimédia e pesquisa e outros serviços.

### 📚 Conclusão
  O portal da Azure oforece vsrios serviços como alguns não citei nesse resumo, visando cobrir todas as necessidades do cliente numa unica plataforma e permite associar as infraestruras que o cliente já possui para ajudar na redução do custo com o substituição dos meios que já existem. 



--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Resumo do Lab Criando máquinas Virtuais na Azure

  Neste Lab aprendemos sobre os ffactores a ter em conta no momento de criação de uma maquina virtual na Cloud do Azure.

### SLA
  Service Level Agreement (SLA) é um documento que pretende gerir as expectativas do fornecedor de serviços e do cliente, relativamente à qualidade do serviço entregue, medindo e validando se os parâmetros previamente acordados são cumpridos. Para a azure, está muito relacionado com o tempo de disponibilidade de um serviço, informando por quanto tempo um serviço pode ficar indisponivel sem que a gente possa cobrar pelos danos causados.

  Abaixo apresento uma tabela que demonstra o tempo de indisponibilidade normal de um serviço de acordo com tipo de SLA:

| Tipos de SLA |Tempo de inatividade por semana |	Tempo de inatividade por mês |	Tempo de inatividade por ano |
|-------|--------|-------------|-----------|
|99% |	1,68 hora |	7,2 horas	| 3,65 dias |
|99,9%	| 10,1 minutos	| 43,2 minutos |	8,76 horas |
|99,95%	| 5 minutos |	21,6 minutos |	4,38 horas |
|99,99%	| 1,01 minuto |	4,32 minutos |	52,56 minutos |
|99,999%	| 6 segundos |	25,9 segundos |	5,26 minutos |

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

### Conclusão
  Ao criar uma maquina virtual, devemos levarem conta as necessidades de uso da mesma. Todo e qualquer recurso configurado resultará no valor da factura após o uso que nos obriga verificar detalhadamente as necessidades do projeto de modo a evitar gastos excessivos o que nos remete a necessidade de avaliação do projecto por arquiteto em nuvem.
