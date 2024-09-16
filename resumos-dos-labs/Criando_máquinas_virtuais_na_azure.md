## Esse resumo do lab é sobre a aula da criação de máquinas virtuais na Azure. 
Nessa aula, a professora reforçou o que é SLA. Irei discutir um pouco mais a fundo sobre esse assunto logo abaixo, visto que é um conceito muito importante na área que atuo, que é SRE:

Um SLA (acordo de nível de serviço) é um acordo entre o provedor e o cliente sobre métricas mensuráveis, como disponibilidade, capacidade de resposta e responsabilidades.
Em geral, esses acordos são elaborados pelas equipes novas de negócios e jurídicas de uma empresa e representam as promessas que você faz aos clientes e as consequências se você não cumpri-las. As consequências incluem penalidades financeiras, créditos de serviço ou extensões de licença.

O SLO (objetivo de nível de serviço) é um acordo dentro de um SLA sobre uma métrica específica, como disponibilidade ou tempo de resposta. Portanto, se o SLA for o acordo formal entre você e o cliente, os SLOs são as promessas individuais que você faz a esse cliente. Os SLOs são o que definem as expectativas do cliente e dizem às equipes de TI e DevOps quais metas precisam atingir e considerar como referência.

O SLI (indicador de nível de serviço) mede a conformidade com o SLO (objetivo de nível de serviço). Assim, por exemplo, se o SLA especificar que os sistemas vão estar disponíveis 99,95% do tempo, é provável que o SLO vá ter 99,95% de disponibilidade, e o SLI é a medição real da disponibilidade. Talvez seja 99,96%. Talvez 99,99%. Para se manter em conformidade com o SLA, o SLI vai precisar cumprir ou superar as promessas feitas nesse documento.

Além deles, também existe o Error Budget, que depende fortemente dessas métricas. Porém não foi o foco da aula.

Também foi visto sobre algumas compute offerings da Azure, e um pouco da interface na criação de VMs.
