# Resumo do Lab: Criação de Máquinas Virtuais na Azure

## Introdução

Esse resumo é sobre a aula de criação de máquinas virtuais na Azure. Durante a aula, a professora reforçou um conceito muito importante na área de **SRE** (Site Reliability Engineering): **SLA** (Acordo de Nível de Serviço). 

Abaixo, discutirei esse conceito e seus componentes relacionados, como **SLO** (Objetivo de Nível de Serviço) e **SLI** (Indicador de Nível de Serviço), que são fundamentais para a confiabilidade dos serviços em cloud.

---

## SLA (Service Level Agreement)

Um **SLA** é um acordo formal entre o provedor de serviços e o cliente, definindo métricas mensuráveis como:

- **Disponibilidade** (uptime do serviço)
- **Capacidade de resposta**
- **Responsabilidades** de ambas as partes

Esses acordos são elaborados geralmente pelas equipes de negócios e jurídicas da empresa, representando as promessas feitas aos clientes e as consequências de não cumpri-las. As consequências podem incluir:

- Penalidades financeiras
- Créditos de serviço
- Extensões de licença

---

## SLO (Service Level Objective)

Um **SLO** é um objetivo específico dentro do SLA. Ele define metas mensuráveis, como:

- **Disponibilidade**
- **Tempo de resposta**

Se o SLA é o acordo formal entre você e o cliente, os SLOs são as promessas específicas que você faz ao cliente. Eles definem as expectativas e indicam às equipes de TI e DevOps quais metas precisam ser atingidas.

---

## SLI (Service Level Indicator)

O **SLI** é a métrica que mede a conformidade com o SLO. Ou seja, se o SLA exige 99,95% de disponibilidade, o SLO vai estipular essa meta, e o SLI será a medição real dessa disponibilidade. Por exemplo:

- O SLO exige 99,95% de disponibilidade
- O SLI mede se o serviço está em conformidade, talvez indicando uma disponibilidade de 99,96% ou 99,99%

Para cumprir o SLA, o SLI precisa atingir ou superar as promessas feitas no acordo.

---

## Error Budget

Embora não tenha sido o foco da aula, vale mencionar o **Error Budget**, que está diretamente relacionado ao SLA, SLO e SLI. Ele define a margem de erro permitida antes de violar um SLO, oferecendo um equilíbrio entre inovação e estabilidade.

---

## Compute Offerings da Azure

Além dos conceitos de SLA, SLO e SLI, a aula também abordou algumas ofertas de computação da Azure, com um foco na criação de **Máquinas Virtuais (VMs)** e na familiarização com a interface da plataforma.

---

Espero que esse resumo tenha ajudado a esclarecer a importância do SLA e seus componentes para garantir a confiabilidade dos serviços em nuvem, especialmente no contexto de **SRE**.
