
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
