# Lab - Armazenamento no Azure

Neste laboratório, exploramos as funcionalidades essenciais do serviço de armazenamento no Azure. A seguir, estão os principais tópicos abordados e os passos realizados:

### 1. Nome da Conta de Armazenamento
- Criamos uma **conta de armazenamento**, cujo nome deve ter entre **3 a 24 caracteres**.
- Esse nome deve ser único globalmente, pois ele será utilizado para identificar os recursos de armazenamento na nuvem.

### 2. Redundância do Armazenamento
- Uma das principais escolhas ao criar uma conta de armazenamento no Azure é a configuração da **redundância**, que define como os dados são replicados para garantir alta disponibilidade e durabilidade. As opções incluem:

  - **LRS (Locally Redundant Storage)**: 
    - Mantém três cópias dos seus dados dentro de um único datacenter na região em que a conta foi criada.
    - É a opção mais econômica, mas oferece menor proteção contra falhas regionais.
  
  - **ZRS (Zone-Redundant Storage)**: 
    - Mantém três cópias dos dados em diferentes zonas de disponibilidade dentro da mesma região, protegendo contra falhas de zona.
  
  - **GRS (Geo-Redundant Storage)**: 
    - Replica seus dados para outra região distante, mantendo seis cópias no total: três na região principal e três na região secundária. 
    - Oferece proteção contra falhas regionais, mas o acesso à réplica secundária só ocorre em caso de desastre.

  - **RA-GRS (Read-Access Geo-Redundant Storage)**: 
    - Similar ao GRS, mas permite leitura da região secundária, mesmo que a região principal ainda esteja funcionando. 

  A escolha da redundância deve ser feita com base no nível de tolerância a falhas e no custo que você está disposto a investir.

### 3. Seleção de Blobs: Acessos Quente ou Frio
- Durante a configuração do **Blob Storage**, optamos por definir a **camada de acesso**:
  - **Quente**: Otimizado para dados acessados frequentemente, com custo de armazenamento mais alto e custo de acesso mais baixo.
  - **Frio**: Ideal para dados que são acessados raramente. O custo de armazenamento é mais baixo, porém o custo de leitura é mais alto.

### 4. Compartilhamento de Arquivos
- Configuramos o **compartilhamento de arquivos** no Azure Storage, possibilitando o armazenamento de arquivos que podem ser acessados por múltiplos usuários e dispositivos. Esse recurso é especialmente útil para cenários de colaboração e migração de sistemas legados para a nuvem.

### 5. Migrações para o Azure
- No laboratório, exploramos a migração de dados locais para o Azure utilizando ferramentas de sincronização, como o **AzCopy**, e processos automatizados, destacando as melhores práticas para mover grandes volumes de dados para a nuvem.

### 6. Utilizando o AzCopy
- A ferramenta **AzCopy** foi usada para realizar a transferência de arquivos de forma rápida e eficiente. O fluxo seguido foi:
  - Criamos uma **Storage Account** → Dentro dela, criamos um **Container** → Geramos um **token SAS** (Shared Access Signature) para acessar o container de forma segura.
  - Com isso, conseguimos copiar arquivos do sistema local diretamente para o **endereço Blob** no Azure.
