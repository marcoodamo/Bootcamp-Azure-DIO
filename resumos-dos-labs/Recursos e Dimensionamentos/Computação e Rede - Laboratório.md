# Criação de Máquina Virtual no Azure

Neste guia, vamos revisar o processo de criação de uma máquina virtual no Azure, abordando conceitos importantes como elasticidade, VMs com desconto Spot, opções de disco, configuração de rede e uso de extensões.

## Passos para a Criação da VM

### 1. Criação da Máquina Virtual

- Primeiramente, criamos uma nova **máquina virtual** na plataforma do Azure. No processo, precisamos definir algumas informações básicas, como:
  - **Nome da VM**
  - **Região**
  - **Tipo de instância**
  
### 2. Conceitos Importantes

#### Elasticidade
- **Elasticidade** refere-se à capacidade de aumentar ou diminuir recursos conforme a demanda de trabalho. No Azure, podemos facilmente escalar VMs, aumentando ou diminuindo a capacidade de computação dependendo da carga de trabalho.

#### Desconto Spot no Azure
- O **desconto Spot** permite utilizar VMs em momentos de demanda ociosa no Azure com **grandes descontos**. Essas VMs podem ser interrompidas quando a capacidade é necessária por outras cargas de trabalho, o que as torna ideais para workloads que podem ser interrompidos, como testes e cenários não críticos.

### 3. Opções de Disco

- O Azure oferece várias opções de disco para a VM, como:
  - **Disco SSD Gerenciado Premium**: Ideal para aplicações que exigem alta performance de IOPS (operações de entrada/saída por segundo).
  - **Disco Standard HDD**: Opção mais econômica, com menor performance, adequada para workloads menos intensivos.
  - **Discos Ultra**: Fornecem a maior performance e são ideais para cargas de trabalho que exigem baixa latência e alta throughput.
  
  A escolha do tipo de disco deve ser feita com base nas necessidades do aplicativo ou serviço que será executado na VM.

### 4. Configuração de Rede

- Algumas opções a serem configuradas incluem:
  - **VNet (Rede Virtual)**: Rede lógica onde a máquina virtual estará conectada.
  - **Sub-rede**: Subdivisão da VNet onde a VM ficará alocada.
  - **Endereço IP público**: Necessário para acessos externos.
  - **Grupo de Segurança de Rede (NSG)**: Define as regras de firewall que controlam o tráfego de entrada e saída da VM. Por exemplo, pode-se configurar quais portas serão abertas, como a porta 22 para SSH ou 3389 para RDP.

### 5. Extensões

- O Azure permite a instalação de **extensões** na VM. As extensões são ferramentas que automatizam tarefas administrativas, como:
  - **Extensão do Docker**: Para instalar e configurar o Docker automaticamente na VM.
  - **Extensão do Custom Script**: Permite executar scripts personalizados, como scripts de inicialização.
  - **Extensão de Diagnóstico**: Utilizada para monitorar e capturar logs de desempenho e eventos da VM.


---
