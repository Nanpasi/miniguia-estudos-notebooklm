# Glossário Git

## Conceitos Fundamentais
* **Git**: É um sistema de controle de versão distribuído (DVCS) de código aberto que rastreia mudanças em arquivos e coordena o trabalho entre várias pessoas

* **GitHub**: Um serviço de hospedagem na web para projetos que utilizam o Git, permitindo colaboração, download de código e gerenciamento de projetos

* **Repositório (Repository)**: O "container" ou pasta onde o Git armazena todo o código de um projeto específico e seu histórico de versões

* **Commit**: Um registro permanente (snapshot) do estado dos seus arquivos em um determinado momento no histórico.
Cada commit possui uma mensagem descritiva e um identificador único

* **SHA-1 (Hash)**: Um identificador único de 40 caracteres (checksum) gerado pelo Git para cada commit e objeto, garantindo a integridade dos dados

## Fluxo de Trabalho e Estados
* **Working Directory (Diretório de Trabalho)**: O local no seu computador onde você edita os arquivos do projeto antes de salvá-los no Git

* **Staging Area (Área de Estágio ou Index)**: Um arquivo ou espaço intermediário onde você marca e prepara as mudanças que serão incluídas no próximo commit

* **Modified (Modificado)**: O estado de um arquivo que foi alterado no diretório de trabalho, mas cujas mudanças ainda não foram salvas no banco de dados do Git

* **Staged (Preparado)**: O estado de um arquivo modificado que foi marcado para ir na próxima foto (snapshot) do commit

## Ramificação e Integração
* **Branch (Ramo)**: Um ponteiro móvel e leve para um commit, permitindo que você divirja da linha principal de desenvolvimento para trabalhar em novas funções isoladamente

* **HEAD**: Um ponteiro especial que indica em qual branch ou commit você está trabalhando no momento dentro do seu repositório local

* **Merge (Mesclagem)**: O ato de combinar o histórico de uma branch específica na sua branch atual

* **Conflict (Conflito)**: Ocorre durante um merge quando a mesma parte de um arquivo foi modificada de formas diferentes em duas branches, exigindo resolução manual

* **Rebase**: Uma forma de integrar mudanças de uma branch para outra, reaplicando os commits sobre uma nova base para manter um histórico mais limpo

## Colaboração e Remotos
* Remote (Remoto): Versões do seu projeto que estão hospedadas na internet ou em uma rede, como no GitHub, para fins de colaboração

* **Clone**: O processo de baixar uma cópia completa de um repositório remoto para o seu computador local, incluindo todo o histórico

* **Fetch**: Baixa os dados e o histórico do repositório remoto para a sua máquina local, mas sem mesclá-los com o seu trabalho atual

* **Pull**: Uma combinação dos comandos fetch e merge; ele baixa as mudanças do servidor e as incorpora automaticamente ao seu código local

* **Push**: O ato de enviar seus commits locais para um repositório remoto, compartilhando suas alterações com outros

* **Fork**: Uma cópia pessoal de um repositório de outra pessoa na sua própria conta do GitHub, facilitando contribuições

* **Pull Request (PR)**: Uma ferramenta do GitHub para solicitar que o dono de um repositório integre mudanças que você fez em sua cópia (fork) ou branch para o projeto principal

## Utilitários
* **Stash**: Permite guardar temporariamente mudanças não commitadas em uma "pilha" para limpar seu diretório de trabalho rapidamente sem perder o progresso

* **Tag**: Um nome amigável e permanente dado a um ponto específico no histórico, geralmente usado para marcar versões de lançamento (como "v1.0")

* **.gitignore**: Um arquivo de texto que instrui o Git a ignorar arquivos e pastas específicos (como arquivos temporários ou senhas), impedindo que sejam rastreados acidentalmente
