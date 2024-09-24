# Estrutura de Contas, Assinaturas e Grupos de Gerenciamento no Azure

- **Conta e Assinaturas**:
  - Uma **conta** pode ter várias **assinaturas**, mas cada **assinatura** pode estar associada a apenas uma **conta**.
  - Cada **assinatura** tem um único **dono** responsável.
  - A Microsoft gera um **relatório de cobrança** para cada assinatura.
  - **Grupos de recursos** são atrelados diretamente às **assinaturas**.

- **Gerenciamento de Acesso e Recursos**:
  - A assinatura permite **gerenciar** e **controlar o acesso** aos recursos que os usuários podem provisionar.
  - O acesso aos recursos é controlado por meio de assinaturas específicas, permitindo melhor governança.

- **Grupos de Gerenciamento**:
  - Quando uma ou mais assinaturas precisam ser organizadas de forma hierárquica, elas são atribuídas a **Grupos de Gerenciamento**.
  - As **regras** e **políticas** definidas no **grupo de gerenciamento** são herdadas por todas as assinaturas pertencentes a esse grupo.
