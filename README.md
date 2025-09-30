# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

Em resumo, até o momento no desenvolvimento do lab foi apresentado e reproduzido no portal:

# Primeiros passos
- Criação de uma conta no azure
- Login de acesso
- Apresentação e navegação na tela inicial pós-login no azure
- Como alterar configurações de idioma e definições de aparência da conta
- Como navegar nas categorias dos recursos

# Criando recursos
- Entendendo SLAs
- Primeiro contato com a criação de máquinas virtuais e suas respectivas opções (quais as implicações no SLA do recurso e seu respectivo custo)
- Primeiro contato com a criação de storages e suas respectivas opções (quais as implicações no SLA do recurso e seu respectivo custo)

# Instância de banco de dados
- Primeiro contato com a criação de instância de banco de dados no azure

*Importante:

- Não é necessário criar uma vm anteriormente, mas é necessário dar um nome ao "server" da instância
- As opções de acesso ao banco são selecionadas no momento da criação (apenas entra id (antigo active directory), apenas usuário SQL ou ambos)

# Grupo de Recursos
- Criando um grupo de recursos
- Associando recursos criados ao grupo
- Verificando informações do log

# Área virtual
- Pessoal: indicado para usuários que tem um perfil de utilização único (ex.: utilizando um software licenciado)
- Em pool: vários usuário acessam sessões diferentes de um mesmo recurso.

# Functions
- Primeiro contato com a criação de funcions
- Utilizado principalmente quando se é necessário de um recurso a partir de um evento (ou gatilho)

# Armazenamento Azure
- Criar conta de armazenamento
* Importante: Nome da conta deve ter de 3 a 24 caracteres (apenas letras minúsculas e números) únicos globalmente

* Tipos de Armazenamento
- Blob: qualquer tipo de arquivo não estruturado
- Files: Pastas/unidades para mapeamento
- Discos do Azure: Discos virtuais
- Filas: Mensagens de até 64kb
- Tabelas: Dados estruturados

* Tipos de replicação
- LRS: Replicação local
- ZRS: Replicação por zona
- GRS: Replicação geográfica
- ZGRS: Replicação por zona geográfica

* Migração para o Azure
- Import/Export Job: Dados > 1TB em diante
- Data Box Disk: Até 35TB
- Data Box: Até 80TB
- Data Box Heavy: Até 800TB

* Ferramentas 
- AzCopy: Via prompt de comando (Tráfego unilateral) - Win, Mac e linux
- Gerenciador de arquivos: Mesmo do AzCopy, mas com interface gráfica - Win, mac e Linux

# Controle de acesso e segurança
- Microsoft Entra ID (Antigo Active Directory)
- Entra Connect: Sync de usuários on Promisses ao Entra ID no Azure
- - Usuários criados no Azure não são sync no on-Premises
  - Após sync apenas senhas são atualizadas no on-premises
    
- RBAC: roles por camadas
- Mic Defender

# Custos
- TCO: Utilizado para calcular e comparar possíveis custos de um ambiente local e o mesmo no Azure
- Calculadora Azure: oferece estimativas de custos em recursos Azure
- tags: boas práticas e melhor organização na fatura
- - Não é obrigatório por padrão para criação de recursos
  - Não é herdável
  - É possível criar policies para copiar tags do recurso pai ao filho ou obrigar a inserção na criação
 
# Portal de confiança do Serviço (servicetrust)
- portal da MS que apresenta um overview/ detalhes de padrões/certificações/regulamentos seguidos em todos os serviços da azure

# Políticas
- A políticas são soberanas sobre o nível da conta

# Bloqueio de Recursos
- Read only: congela o status do recurso/grupo
- Delete: impede a exclusão do recurso/grupo

Importante: o bloqueio é herdado pelo recurso filho
Ao mover um recurso de um grupo e o bloqueio for a nível de grupo, o bloqueio não é mantido

# MS Purview
- Portal para analise de governança e conformidade de dados

# Gerenciamento de recursos
Para operações em lote, templates podem ser utilizados, tais instruções serão executadas por: 
- Cloud Shell: PowerShell que conecta ao Azure para execução de instruções
- Azure CLI: mesma coisa do Cloud Shell, mas baseado em bash

- ARM: Camada de interface que interpreta comandos do portal ou de instruções

- Bicep: linguagem amigável para gerenciamento via comandos em contrapartida ao JSON

- ARC: Ferramenta de gerenimento multicloud
