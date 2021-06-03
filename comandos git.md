**Comandos da GIT**

ls (macOS/Linux)
dir (Windows)
-> lista todos os arquivos presentes no diretório atual (macOS/Linux)

mkdir nome-da-pasta 
-> cria uma nova pasta 

cd nome-da-pasta 
-> navega para a pasta especificada (exemplo: cd documentos)

cd .. 
-> sobe um nível de pasta

touch nome-do-arquivo
dir > nome-do-arquivo
-> (nome junto com a  extensão do arquivo) cria um novo arquivo

clear (macOS/Linux)
cls (Windows)
-> limpa todas as informações do terminal

 dir > (no CDM ) = criar um novo arquivo

pwd - mostra o caminho do diretório

esc:q (sai do vim sem salvar)

esc:qw (salva e sai do vim)

--------
git init
-> inicializa o git no repositório local

git add
-> adiciona um arquivo modificado ao stagging (área temporária) 

git status
-> mostra os status dos arquivos modificados

git commit 
-> cria um commit

git commit --amend
-> corrigir mensagem do commit 

git pull
-> puxa as atualizações mais recente (remoto -> local)

git push
-> envia as atualizações mais recentes (local -> remoto)

git remote add origin caminho
-> adiciona o seu repositório local ao remoto

git checkout -- nome-arquivo
-> descarta as alterações locais do arquivo informado

git checkout -b (cria uma branch a partir de onde você esta )

git checkout nomeDaBranch (navega de uma branch para outra)

git config --get remote.origin.url  (mostra qual a url do repositório remoto)

git clone [url]
(é usado para criar uma cópia de um repositório ou branch específico dentro de um repositório.)

Obs:
ctrl + c = sair do modo de edição git

