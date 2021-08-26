# Comandos para versionamento de código com Git

> Veja a seguir alguns dos comandos fundamentais para o controle e o versionamento de códigos em Git.

<br>
<br>

### Comandos:
 - ```git config``` - Usado para definir configurações globais ou relacionadas ao repositório, como:
> ```git config --global user.name "Seu Nome"``` - Define um nome usado para identificação nos commits
<br>
```git config --global user.email seu@email.com``` - Define um email também para a indentificação
<br>
```git config --global init.defaultBranch "nome da branch"``` - Altera o nome de sua branch padrão ao criar um novo repo

O mesmo comando também é usado para a definição de aliases, define configurações nas branchs, customiza cores dos greps, branchs, logs e etc e muitas outras configurações.

> <a href="https://git-scm.com/docs/git-config">Leia a documentação do comando para mais informações</a>

- ```git init``` - Inicia um repositório vazio em um diretório local em seu computador
- ```git status``` - Lista o status dos arquivos no repositório, indicando quais ainda não foram para o controle de versão
- ```git add``` - Adiciona arquivos ainda não rastreados no diretório pelo ```git status``` para o controle de versão
> Qualquer novo arquivo adicionado em seu diretório local o git por padrão não tem conhecimento dele, por isso existe o comando ```git add```, com este comando um arquivo ainda não rastreado passa a ser reconhecido. Pode-se utilizar o comando de forma padrão: ```git add nome_do_arquivo.extensão``` que adiciona arquivos um a um ou então utilizando ```git add .``` (com o ponto), todos os arquivos serão rastreados.
- ```git commit``` - Grava no repositório os arquivos que já estão rastreados
> Utilizando o parâmetro ```-m``` é definida uma mensagem de idenficação no commit feito, exemplo: ```git commit -m "Mensagem de exemplo```
- ```git log``` - Lista todas as alterações feitas no repositório
- ```git rm nome_arquivo.extensão``` - Remove um arquivo do projeto
- ```git mv nome_arquivo.extensão novo_nome_arquivo.extensão``` - Renomeia um arquivo no projeto
- ```git mv novo_nome_arquivo.extensão pasta/novo_nome_arquivo.extensão``` - Move um arquivo para pastas dentro do projeto
- ```git remote add origin https://github.com/seunome/repositorio.git``` - Aponta o projeto para um repositório remoto
- ```git push``` - Faz o upload do repositório local para um repositório remoto no GitHub, levando em conta apenas os arquivos rastreados e já "commitados"
> O comando necessita de parâmetros como qual o repositório para enviar os arquivos (normalmente é definido como ```origin``` em ```git remote add```) e precisa também saber em qual branch os arquivos serão enviados (geralmente ```master```), ficando: ```git push origin master```
- ```git clone https://github.com/usuario/repositorio.git``` - Clona um repositório já existente no ambiente local com a origem configurada
- ```git remote``` - Exibe o nome do repositório remoto
- ```git remote -v``` - Exibe o nome e a url do repositório remoto
- ```git remote rename nome-repositorio novo-nome``` - Renomeia o repositório remoto
- ```git remote set-url nome-repositorio https://github.com/seunome/repositorio.git``` - Altera a url do repositório remoto
- ```git pull``` - Sincroniza os arquivos de um repositório local com os de um remoto, puxando os arquivos inexistentes
- ```git branch nome-branch``` - Cria uma nova branch (um novo diretório que contém o mesmo conteúdo das outras mas ao ser modificado, não reflete as mudanças)
- ```git branch``` - Lista as branches do repositório local
- ```git checkout nome-branch``` - Alterna de uma branch para outra
- ```git branch -d nome-branch``` - Apaga a branch e todo o seu conteúdo
- ```git merge nome-branch -m "Mensagem"``` - Traz as modificações de uma branch para a branch atual
- ```git branch --no-merged``` - Verifica quais branchs ainda não tem seus conteúdos mesclados com a branch atual