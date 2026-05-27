<p>(<mark><i>Resumo estruturado feito pelo NotebookLM</i></mark>)</p>
<hr>

# 1. O que são Git e GitHub?
**Git**: É um sistema de controle de versão distribuído (DVCS) gratuito e de código aberto
Ele registra as mudanças feitas em arquivos ao longo do tempo, permitindo que você recupere versões específicas e trabalhe simultaneamente com outras pessoas sem que o trabalho de um sobrescreva o do outro
Foi criado por Linus Torvalds em 2005 para o desenvolvimento do kernel do Linux

**GitHub**: É um serviço de hospedagem na web para projetos que utilizam o Git
Enquanto o Git é o que você faz localmente no seu computador, o GitHub é onde o trabalho é armazenado publicamente (ou privadamente) em um servidor para colaboração

# 2. Os Três Estados do Git
Para entender o Git, é crucial compreender os três estados em que um arquivo pode estar
:  
  
* **Modified** (Modificado): Você alterou o arquivo, mas ainda não salvou a alteração no banco de dados do Git

* **Staged** (Preparado/Área de Estágio): Você marcou um arquivo modificado em sua versão atual para ir na próxima foto (snapshot) do commit
A Staging Area (também chamada de "index") é um arquivo que armazena informações sobre o que irá no próximo commit

* **Committed** (Confirmado): Os dados estão armazenados de forma segura no seu diretório Git local

# 3. Configuração Inicial e Primeiros Passos
Após instalar o Git
, o primeiro passo é configurar sua identidade, o que será associado aos seus commits
:  
```git config --global user.name "Seu Nome"```  
```git config --global user.email "seuemail@exemplo.com"```
# 4. Fluxo de Trabalho Comum (Comandos Essenciais)
git init: Transforma um diretório local comum em um repositório Git

* ```git clone [url]```: Cria uma cópia local completa de um repositório remoto, incluindo todo o histórico

* ```git add [arquivo]```: Adiciona arquivos à área de estágio (staging area) para serem incluídos no próximo commit

* ```git commit -m "mensagem"```: Grava permanentemente o snapshot dos arquivos da área de estágio no histórico

* ```git status```: Mostra o estado atual do seu diretório de trabalho e da área de estágio (quais arquivos estão modificados, preparados ou não rastreados)

* ```git log```: Lista o histórico de versões/commits do projeto em ordem cronológica reversa

# 5. Ramificação (Branching) e Mesclagem (Merging)
Uma **branch** no Git é um ponteiro móvel e leve para um commit
Elas permitem que você saia da linha principal de desenvolvimento para trabalhar em novas funcionalidades sem interferir no código estável

* ```git branch [nome]```: Cria uma nova branch

* ```git checkout [branch]``` ou ```git switch [branch]```: Muda para a branch especificada

* ```git merge [branch]```: Combina o histórico de uma branch na branch atual em que você está

# 6. Colaboração e Repositórios Remotos
Para trabalhar com outras pessoas, você interage com servidores remotos (como o GitHub)
:
* ```git remote add [nome] [url]```: Conecta seu repositório local a um servidor remoto

* ```git push [remoto] [branch]```: Envia seus commits locais para o servidor remoto

* ```git pull```: Baixa as mudanças do servidor e as incorpora automaticamente ao seu código local

# 7. Colaboração no GitHub (GitHub Flow)
O GitHub facilita a colaboração através de ferramentas visuais
:  


* **Fork**: Você cria uma cópia pessoal de um projeto de outra pessoa em sua conta do GitHub

* **Pull Request (PR)**: Após fazer melhorias em sua cópia, você solicita que o dono original do projeto "puxe" suas mudanças para o projeto principal
Isso permite a revisão de código e discussão antes da integração final
