# 🔐 Segurança e Governança no Azure

A segurança e governança de dados são elementos essenciais em qualquer solução de nuvem, e a Microsoft oferece diversas ferramentas e mecanismos para garantir que os dados estejam protegidos, e as operações sejam realizadas de acordo com as melhores práticas e regulamentações.

## 📜 Service Trust da Microsoft

O **Microsoft Service Trust** oferece um conjunto abrangente de informações, recursos e relatórios que ajudam as organizações a entenderem como a Microsoft protege a segurança e a conformidade dos seus serviços de nuvem. O portal **Service Trust** fornece:

- Documentação detalhada sobre conformidade regulatória.
- Relatórios de auditorias de segurança.
- Informações sobre as práticas de segurança e privacidade da Microsoft.
- Ferramentas que auxiliam as organizações a gerenciar seus requisitos de conformidade com base nos serviços da Microsoft.

🔍 **Na prática**, esse portal é essencial para empresas que precisam validar o cumprimento de regulamentações como **GDPR**, **HIPAA**, e outras normas, utilizando os serviços Microsoft de maneira segura e em conformidade.

## 🔒 Bloqueios a Nível de Resource Group

No Azure, é possível aplicar **bloqueios** a recursos e **resource groups** para proteger o ambiente contra alterações acidentais ou exclusões não intencionais. Existem dois tipos principais de bloqueios:

- **Read-Only**: Impede todas as modificações nos recursos, permitindo apenas a leitura. Quando aplicado, **não permite a movimentação** de recursos entre resource groups.
- **Excluir**: Permite a leitura e modificação dos recursos, mas **bloqueia a exclusão**. Mesmo com esse bloqueio, ainda é possível **mover recursos** entre diferentes resource groups.

💡 **Dica**: Se você deseja proteger recursos contra exclusão, mas ainda permitir alterações e movimentação de recursos, o bloqueio de exclusão é o ideal. O bloqueio Read-Only é mais restritivo, sendo útil em ambientes de produção críticos.

## 🗂️ Microsoft Purview

O **Microsoft Purview** é uma plataforma unificada de governança de dados que ajuda as organizações a gerenciar, proteger e descobrir seus dados de forma eficaz, independentemente de onde estejam armazenados – seja em ambientes locais, na nuvem, ou em sistemas SaaS. Algumas de suas funcionalidades principais incluem:

- **Catálogo de Dados**: Descubra e classifique seus dados de maneira centralizada.
- **Mapeamento de Origem**: Identifique a origem dos dados e seu ciclo de vida.
- **Políticas de Governança**: Defina e aplique políticas de segurança e privacidade para garantir o compliance.
- **Relatórios de Auditoria**: Monitore o uso dos dados e crie relatórios de conformidade.

🚀 **Na prática**, o Purview permite que empresas gerenciem e monitorem os dados de forma eficiente, garantindo conformidade com regulamentações de privacidade e segurança de dados em todos os ambientes.

## 🛡️ Azure Policies

As **Azure Policies** são utilizadas para garantir que os recursos em um ambiente Azure estejam em conformidade com as regras e padrões da organização. As Policies permitem:

- **Aplicar regras** para garantir que recursos atendam aos requisitos de conformidade.
- **Monitorar a conformidade** de forma contínua e remediar recursos que estejam fora de conformidade.
- **Automatizar ações**, como a aplicação de tags, bloqueio de determinados tipos de recursos, ou a exigência de configurações de segurança específicas.

As Policies podem ser aplicadas a diferentes níveis: assinatura, resource groups ou diretamente aos recursos.

💡 **Exemplo**: Você pode criar uma policy para garantir que todas as máquinas virtuais sejam implantadas apenas em regiões específicas, ou que um conjunto de tags seja obrigatório em todos os novos recursos.

---
*💡 Dica final:* A governança proativa, com o uso das Policies e bloqueios, em conjunto com a visibilidade e controle proporcionados pelo Purview, pode ajudar a evitar problemas futuros e garantir um ambiente seguro e eficiente.
