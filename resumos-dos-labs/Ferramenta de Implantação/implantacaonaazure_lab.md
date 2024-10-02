# ☁️ Ferramentas e Automação no Azure

A Microsoft Azure oferece diversas ferramentas para automação, gestão de ambientes e desenvolvimento de infraestrutura como código (IaC), tornando mais simples e eficiente o gerenciamento de recursos em nuvem e ambientes híbridos.

## 💻 Cloud Shell

O **Azure Cloud Shell** é um terminal baseado em navegador que permite a administração dos recursos do Azure diretamente a partir do portal. Ele suporta tanto **Bash** quanto **PowerShell** e vem com várias ferramentas integradas, como:

- **CLI do Azure**: Interface de linha de comando para gerenciar os recursos.
- **PowerShell**: Scripts poderosos para automação e administração.
- **Git**: Controle de versão para gerenciar scripts e arquivos.
- **Ferramentas de DevOps**: Como Terraform, Ansible, e Kubernetes.

☁️ **Na prática**, o Cloud Shell permite que os administradores gerenciem seus recursos sem precisar configurar ferramentas localmente. Ele já vem com permissões associadas à sua conta do Azure, tornando o processo de administração mais rápido e prático.

## 🔄 Automação (CLI / PS; Tasks; Export Template)

A **automação** no Azure é essencial para escalar operações e garantir a consistência das configurações. Existem várias maneiras de automatizar tarefas no Azure:

- **CLI e PowerShell**: Através da CLI do Azure ou PowerShell, é possível criar scripts para automatizar tarefas repetitivas como provisionamento de VMs, gerenciamento de redes e orquestração de recursos.
  
- **Tasks**: O Azure também permite a criação de **Runbooks** dentro do **Azure Automation** para agendar tarefas, como backups automáticos, monitoramento e remediação de alertas. Isso pode ser feito através de PowerShell ou scripts Python.

- **Export Template**: Sempre que um recurso é criado no portal, você pode exportar a definição dele como um template **ARM (Azure Resource Manager)**. Isso permite que o mesmo recurso seja recriado ou modificado de forma padronizada.

## 📜 Bicep e Bicep Playground

O **Bicep** é uma linguagem declarativa usada para implementar recursos no Azure de maneira mais simples e limpa em comparação com os templates ARM tradicionais. Ele oferece uma sintaxe mais concisa e é projetado para ser fácil de usar, enquanto ainda fornece todos os recursos e integrações disponíveis com o ARM.

### 🌐 Bicep Playground
O **Bicep Playground** é uma plataforma online que permite experimentar o Bicep diretamente no navegador. Nele, você pode escrever templates em Bicep, ver a tradução para o ARM correspondente, e aprender as melhores práticas para construir infraestruturas de nuvem.

- Acesse o Bicep Playground: https://aka.ms/bicepdemo

## 🌍 Azure Arc

O **Azure Arc** é uma solução que expande os serviços e o gerenciamento do Azure para qualquer infraestrutura, seja ela on-premise, em múltiplas nuvens ou até mesmo em dispositivos de borda (edge). Com o Azure Arc, você pode:

- **Gerenciar servidores**: Adicionar servidores físicos ou virtuais ao Azure, permitindo que eles sejam gerenciados como recursos nativos da nuvem.
- **Gerenciamento Kubernetes**: Unificar a gestão de clusters Kubernetes, independente de onde estejam.
- **Gerenciar dados**: Estender serviços de dados do Azure, como SQL Managed Instance, para ambientes fora da nuvem.
- **Aplicar políticas e compliance**: Usar as mesmas Azure Policies em ambientes híbridos para garantir a conformidade em todos os cenários.

🌐 **Na prática**, o Azure Arc permite que você traga a gestão centralizada do Azure para qualquer lugar, facilitando o controle e a visibilidade de ambientes híbridos complexos.

---
*💡 Dica final:* Explorar o **BicepPlayground** e automatizar tarefas usando a CLI ou PowerShell são ótimos pontos de partida para gerenciar eficientemente seus recursos no Azure.

## CLI p/ criar uma VM
```
az vm create --resource-group MeuGrupo --name MinhaVM --image UbuntuLTS
```
## Exemplo Bicep
```
resource vm 'Microsoft.Compute/virtualMachines@2021-03-01' = {
  name: 'MinhaVM'
  location: 'eastus'
  properties: {
    hardwareProfile: {
      vmSize: 'Standard_DS1_v2'
    }
    osProfile: {
      computerName: 'MinhaVM'
      adminUsername: 'adminuser'
      adminPassword: 'SenhaForte123!'
    }
  }
}
