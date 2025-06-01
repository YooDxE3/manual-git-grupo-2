Comandos Básicos do Git
1. Configuração Inicial
git config --global user.name "Seu Nome"
Define o nome do usuário para todos os repositórios locais.

git config --global user.email "seuemail@example.com"
Define o e-mail do usuário para todos os repositórios locais.

git config --global core.editor nome_editor
Define o editor de texto padrão para o Git (por exemplo, vim, nano, code).


2. Inicialização e Clonagem de Repositórios
git init
Inicializa um novo repositório Git no diretório atual.

git clone URL
Clona um repositório remoto existente para o seu ambiente local.


3. Verificação do Status
git status
Exibe o estado atual do repositório, mostrando arquivos modificados, adicionados ou não rastreados.


4. Adição e Confirmação de Alterações
git add arquivo
Adiciona um arquivo específico à área de preparação (staging area).

git add .
Adiciona todas as alterações no diretório atual à área de preparação.

git commit -m "mensagem"
Confirma as alterações adicionadas com uma mensagem descritiva.


5. Histórico de Commits
git log
Exibe o histórico de commits do repositório.



6. Trabalhando com Branches
git branch
Lista todas as branches locais.

git branch nome_da_branch
Cria uma nova branch com o nome especificado.

git checkout nome_da_branch
Alterna para a branch especificada.

git checkout -b nome_da_branch
Cria e alterna para uma nova branch.

git merge nome_da_branch
Mescla a branch especificada à branch atual.


7. Interação com Repositórios Remotos
git remote add origin URL
Adiciona um repositório remoto com o nome "origin".

git push origin nome_da_branch
Envia os commits da branch local para o repositório remoto.

git pull origin nome_da_branch
Atualiza a branch local com as alterações do repositório remoto.

8. Desfazendo Alterações
git restore arquivo
Restaura o arquivo para o último estado confirmado.

git reset --hard HEAD
Descarta todas as alterações não confirmadas, revertendo para o último commit.

git revert hash_do_commit
Cria um novo commit que desfaz as alterações do commit especificado.

9. Ignorando Arquivos
.gitignore
Arquivo onde você especifica padrões de arquivos ou diretórios que o Git deve ignorar.
