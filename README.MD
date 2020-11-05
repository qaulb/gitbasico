# Universidade QA
Estudando **Git básico**
---
## Resumo projeto
Criado para demostrar conhecimento em Git básico.
---
## Criando um novo repositório
1 - Crie uma nova pasta, abra-a com o gitbash ou terminal escolhido e execute o comando **(git init)** para criar um novo repositório.
---
## Obtendo um repositório clonando:
1 - Crie uma cópia de trabalho em um repositório local executando o comando<br> **(*git clone /caminho/para/o/repositório*)**
caminho do projeto no próprio Github.<br>
Quando usar um servidor remoto, seu comando será: **(*git clone usuário@servidor:/caminho/para/o/repositório*)**
---
## Fluxo de trabalho Git
Seus repositórios locais consistem em três "árvores" administradas pelo git na seguinte ordem:
> Working Directory -  que contém os arquivos vigentes.<br>
> Index (stage) - que funciona como uma área temporária alocando suas alterações.<br>
> HEAD - que aponta para o último commit (confirmação) que você fez.<br>
---
## Adicionando e Confirmando alterações
1 - Após propor mudanças e alterações em um projeto, você deve adicioná-las ao (Index) usando:<br>
**(git add <arquivo>)** - para um arquivo em específico<br>
**(git add .)**  para todos as alterações.<br>
> Este é o primeiro processo do fluxo de trabalho básico do git.
2 - Para realmente confirmar as mudanças (commit) digite o comando: **(*git commit -m "alterações resumidas"*)**.
Os arquivos serão enviados para a (HEAD), porém ainda não estarão no repositório remoto.
---
## Enviando as alterações
1 - Com as alterações no (HEAD) da sua cópia de trabalho local. Para enviar as alterações ao seu repositório remoto, execute
**(git push origin master)**<br>
> Altere a master para qualquer ramo (branch) desejado, enviando suas alterações.
Caso não tenha clonado um repositório existente e quer conectar seu repositório a um servidor remoto, adicione com
**(git remote add origin <servidor>)** agora você pode enviar suas alterações para o servidor remoto escolhido.
---
## Trabalhando com Ramificações
> Branches **("ramos")** são utilizados para desenvolver funcionalidades separadas entre si.<br>
(A master é o branch "padrão" quando você cria um repositório.)
> Sempre use outros branches para desenvolver e não **"cagar"** a master de um projeto, logo depois mescle-os (merge) ao branch master após a conclusão dos trabalhos.
1 - Crie e selecione um novo branch chamado "funcionalidade_x" usando: **(*git checkout -b funcionalidade_x*)**
2 - Caso queira retorne para o master usando **(*git checkout master*)**
3 - Se quiser remova o branch da seguinte forma **(*git branch -d funcionalidade_x*)**
(Um branch não fica disponível a outros a menos que você envie ao seu repositório remoto com **(*git push origin <funcionalidade_x>*)**
---
## Atualizando e Mesclando
1 - Caso deseje atualizar seu repositório local com a mais nova versão que tenha ajustes de outros Devs, execute<br>
 **(git pull)** na sua pasta de trabalho para obter e fazer merge (mesclar) alterações remotas.
2 - Para fazer merge de algum branch ao seu branch ativo (ex. master), use **(git merge <nome do branch>)**,
em ambos os casos o git tenta fazer o merge das alterações automaticamente.
> Infelizmente, nem sempre é possível e causa conflitos. Resolva os conflitos manualmente exibido pelo git em seu editor preferido para fazer o merge destes conflitos.
3 - Depois de alterar, você precisa marcá-los como merged com **(git add <arquivo>)** antes de fazer o merge das alterações, você pode também pré-visualizá-as usando **(git diff <branch origem> <branch destino>)**
---
  
### Créditos de estudo:
> Curso Udemy: https://www.udemy.com/course/git-e-github/<br>
> FOLHA DE DICAS DE GIT: https://training.github.com/downloads/pt_BR/github-git-cheat-sheet.pdfv
