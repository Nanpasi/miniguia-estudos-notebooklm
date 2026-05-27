# miniguia-estudos-notebooklm
<p><mark><i>Projeto/atividade do Bootcamp Afya - Automação de Dados com IA</i></mark></p>

# Assunto: Git
"Este guia técnico funciona como uma folha de dicas essencial para o uso do Git, um sistema de controle
de versão distribuído amplamente utilizado. O material detalha comandos fundamentais para configurar
o ambiente, iniciar novos repositórios e gerenciar o fluxo de trabalho diário de um desenvolvedor."
_Descrição do caderno temático gerado pelo próprio modelo de linguagem do NotebookLM._

O objetivo desse caderno temático é servir como um guia auxiliar prático para quem está procurando se
aprofundar ou começar a utilizar o Git.

Através dele tenho como objetivo aprender todos os comandos básicos de Git e como usá-los de maneira eficiente para trabalhar em projetos do GitHub de maneira profissional e otimizada.

# Perguntas
## "Como faço para criar um repositório no GitHub usando o Git? Me mostre um passo a passo."
Para criar um repositório no GitHub e conectá-lo ao seu computador usando o Git, você deve seguir um processo que envolve a configuração local, a criação do repositório no site do GitHub e a sincronização entre ambos.  
Aqui está o passo a passo detalhado:
1. **Configure sua Identidade**  
Antes de começar, você precisa configurar seu nome de usuário e e-mail no Git, pois essas informações serão associadas aos seus "commits".
Abra o terminal (ou Git Bash) e use os comandos:
```git config --global user.name "Seu Nome"```.
```git config --global user.email "seuemail@exemplo.com"```.

2. **Inicialize o Repositório Local**  
Navegue até a pasta do seu projeto no computador e transforme-a em um repositório Git.
No terminal, digite: ```git init```.
Isso criará uma pasta oculta chamada _.git_, onde o Git armazenará todo o histórico e metadados do projeto.

3. **Adicione e Comite seus Arquivos**  
Agora, você precisa preparar os arquivos para o primeiro envio.  
Adicione todos os arquivos ao "staging area" (área de preparação): ```git add```.  
Grave a primeira versão (snapshot) dos arquivos: ```git commit -m "Primeiro commit"```.  

4. **Crie o Repositório no GitHub**  
Para hospedar seu código online, você deve criar o "container" no servidor do GitHub.
Acesse github.com e faça login.  
Clique no botão "+" no topo da página e selecione "New repository".  
Dê um nome ao seu repositório e clique em **"Create repository"**.  
Após a criação, o GitHub mostrará uma URL (HTTPS ou SSH). Copie essa URL.  

5. **Conecte o Repositório Local ao Remoto**  
Agora você deve dizer ao seu Git local para onde ele deve enviar os arquivos.  
Use o comando: ```git remote add origin <URL_COPIADA>```.  
O nome "origin" é um apelido padrão para o servidor onde seu código será armazenado.  

6. **Envie (Push) os Arquivos para o GitHub**  
Finalmente, faça o upload dos seus commits locais para o servidor.  
Use o comando: ```git push -u origin master```.  
O parâmetro **-u** faz com que o Git lembre dessa configuração, permitindo que, nas próximas vezes, você use apenas git push.  
Nota: Se você estiver usando uma versão recente do Git, o nome da branch principal pode ser main em vez de master.  
Após esses passos, seu código estará visível no GitHub e pronto para ser compartilhado ou acessado de outros computadores via git clone.  

## "Como funcionam os branches no Git?"
No Git, as **branches** (ramos) funcionam como ponteiros móveis e leves que apontam para commits específicos no histórico do seu projeto.  Elas permitem que você divirja da linha principal de desenvolvimento para trabalhar em novas funcionalidades ou correções sem interferir no código estável.  
Abaixo, detalho o funcionamento técnico e prático das branches:  

1. **A Natureza das Branches**  
Diferente de outros sistemas de controle de versão que copiam arquivos, uma branch no Git é apenas um arquivo simples contendo os 40 caracteres do hash SHA-1 do commit para o qual ela aponta.
Por isso, criar ou excluir uma branch é uma operação quase instantânea.  
    * **Branch Padrão**: Ao inicializar um repositório, o Git cria por padrão uma branch chamada master (ou main).  
    * **Avanço Automático**: Sempre que você faz um novo commit enquanto está em uma branch, o ponteiro dessa branch avança automaticamente para o novo commit.  

2. **O Ponteiro HEAD**  
Para saber em qual branch você está trabalhando no momento, o Git utiliza um ponteiro especial chamado HEAD.  
Quando você usa o comando git checkout ou git switch, o HEAD muda para apontar para a branch selecionada. 
Ao trocar de branch, o Git também atualiza os arquivos no seu diretório de trabalho para que correspondam ao snapshot (versão) daquela branch específica.  

3. **Integração de Mudanças**  
Existem duas formas principais de combinar o trabalho de diferentes branches:  
    * **Merge (Mesclagem)**: Une as histórias de duas branches. Se o commit da branch que você está integrando for um descendente direto da sua branch atual, o Git apenas move o ponteiro para frente (fast-forward).
    Caso as histórias tenham divergido, o Git realiza um three-way merge, criando um novo "commit de merge" que possui dois pais.  
    * **Rebase (Rebaseamento)**: Em vez de criar um commit de merge, o rebase pega todas as mudanças feitas em uma branch e as "reaplica" sobre outra, criando um histórico linear e mais limpo.  

4. **Fluxos de Trabalho Comuns**  
O uso de branches incentiva fluxos de desenvolvimento dinâmicos:
    * **Topic Branches**: São ramos de curta duração criados para uma tarefa específica (como o conserto de um bug ou uma nova ideia), que são descartados após serem mesclados na branch principal.  
    * **Long-Running Branches**: Algumas branches permanecem abertas durante todo o ciclo de vida do projeto, como uma branch master apenas para código estável e uma branch develop para integração de novas funcionalidades.  

5. **Branches Remotas** 
As branches remotas são referências ao estado das branches em repositórios externos (como no GitHub).
Elas agem como marcadores que você não pode mover manualmente; o Git as move automaticamente sempre que você faz uma comunicação de rede (git fetch ou git pull) para garantir que elas representem fielmente o servidor.  
Para gerenciar suas branches locais, os comandos essenciais são git branch (listar ou criar), git checkout ou git switch (alternar) e git merge (combinar).  

## "Qual é a origem do Git? Quando e por que foi criado? E por quem?"
O Git teve uma origem marcada por controvérsia e necessidade técnica dentro da comunidade de desenvolvimento do kernel do Linux.  
Aqui estão os detalhes sobre sua criação:  
* **Quem criou**: O Git foi projetado e desenvolvido por Linus Torvalds, o criador do sistema operacional Linux.  
* **Quando foi criado**: O desenvolvimento começou em abril de 2005. A primeira versão do kernel do Linux gerenciada pelo Git foi lançada em junho de 2005, e a versão 1.0 oficial do Git foi lançada em dezembro do mesmo ano.  
* **Por que foi criado**: Durante muito tempo (1991–2002), o kernel do Linux era mantido apenas através do envio de arquivos compactados e patches.
  Em 2002, o projeto passou a usar um sistema proprietário chamado BitKeeper.
  No entanto, em 2005, a relação entre a comunidade Linux e a empresa proprietária do BitKeeper ruiu, resultando na revogação da licença de uso gratuito da ferramenta.
  Como nenhuma outra ferramenta da época atendia às necessidades de desempenho e fluxo distribuído do Linux, Torvalds decidiu criar sua própria ferramenta.  
* **Os principais objetivos do novo sistema eram**:  
  * Velocidade e eficiência para lidar com projetos grandes como o kernel do Linux;
  * Design simples;
  * Forte suporte ao desenvolvimento não linear, permitindo milhares de ramificações (branches) paralelas;
  * Ser um sistema totalmente distribuído;
  * Garantir a integridade dos dados contra corrupção acidental ou maliciosa.

<p>-> <i><mark>Notei que as respostas do modelo de linguagem são menores sempre que pergunto algo sobre teoria ou história. Isso mostra que maior parte das fontes que peguei
consiste de informações práticas, sem muitos dados e informações cronológicas e históricas.</mark></i></p>

## "Git e GitHub são a mesma coisa? Há alguma diferença entre eles?"
Não, Git e GitHub não são a mesma coisa, embora estejam intimamente relacionados e sejam frequentemente usados juntos.  
De forma simplificada, o Git é a ferramenta (o sistema de controle de versão), enquanto o GitHub é o serviço de hospedagem que utiliza essa ferramenta.  
Aqui estão as principais diferenças entre eles, conforme detalhado nas fontes:  

1. **Natureza e Localização**  
    * **Git**: É um sistema de controle de versão distribuído de código aberto.
    Ele é o fluxo de trabalho (workflow) que você utiliza localmente no seu próprio computador para rastrear mudanças em arquivos e coordenar o trabalho entre várias pessoas.

    * **GitHub**: É uma plataforma de hospedagem na web para projetos que utilizam o Git.
    É o lugar onde o trabalho feito localmente com o Git é armazenado publicamente (ou privadamente) em um servidor remoto.
  
2. **Funcionalidade Principal**  
    * **Git**: Foca no gerenciamento de versões, permitindo que você crie ramificações (branches), faça commits e visualize o histórico de alterações diretamente na sua máquina.  
    * **GitHub**: Além de hospedar os repositórios Git, ele oferece uma interface gráfica e diversas ferramentas sociais e de colaboração que o Git sozinho não possui, como:  
      * **Pull Requests**: Para submissão e revisão de código.
      * **Issue Tracking**: Para relatórios de bugs e gerenciamento de tarefas.  
      * **Wiki e Páginas Web**: Para documentação do projeto.  
      * **Ferramentas de Integração**: Conexão com serviços externos de testes e automação.  

3. **Propriedade e Acesso**  
    * **Git**: É um software livre criado por Linus Torvalds em 2005 para o desenvolvimento do kernel do Linux.
      Você pode usá-lo sem qualquer conta ou conexão com a internet para gerenciar seus projetos locais.  
    * GitHub: É um serviço comercial (propriedade da Microsoft) que requer a criação de uma conta de usuário.
      Ele atua como o ponto central onde milhões de desenvolvedores colaboram em projetos de código aberto.
      
Em resumo, o Git é o motor que faz o controle de versão funcionar, e o GitHub é a garagem e o centro de colaboração onde você guarda seu código e trabalha com outros desenvolvedores.  
Existem outras plataformas similares ao GitHub, como o GitLab, que também utilizam o Git para hospedar projetos.  


## Links das fontes
https://git-scm.com/cheat-sheet.pdf
https://git-scm.com/book/en/v2
https://www.researchgate.net/publication/340528902_A_Beginner's_Guide_to_Git_and_GitHub
https://web.stevens.edu/hfslwiki/images/1/1d/GIT_Tutorial.pdf

---

_O **resumo estruturado** (resumo_estruturado.md), **glossário** (glossario.md) e **prompts reutilizáveis** (prompts_reutilizaveis.md) estão todos disponíveis em arquivos separados dentro do próprio repositório._
