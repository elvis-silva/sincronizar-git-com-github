# Como sincronizar o git local com o github via terminal Linux

Download o git:

    http://git-scm.com/download/linux

Crie uma conta no Github caso não tenha:

    https://github.com/

Execute o seguinte comando no terminal:

    $ ssh-keygen -t rsa -C "seu-email@dominio.com"

ATENÇÃO: Nesse momento ele pedirá usuário e senha, eu não quero ter que ficar digitando login e senha toda vez que fizer um envio para o github, por isso, nessa hora, clique ENTER todas as vezes até ele finalizar a criação da sua KEYGEN.
A chave SSH fica na pasta oculta chamada ".ssh" na sua Pasta Pessoal com o nome de "id_rsa.pub", abra esse arquivo e copie todo seu conteúdo.

Entre no seu Github:

Agora no github, vá em configurações -> SSH Keys -> Add SHH Keys e no título coloque o que quiser, depois em Key cole todo conteúdo do SSH copiado anteriormente, salve as alterações e pronto, você já tem a conexão com seu Github.

Criar repositório no github.com:

Click no botão "New repository" e dê um nome.
Existem 2 tipos de repositórios, públicos (free) e privados (pagos). Escolha o público.
Após criar ele irá mostrar na tela algumas informações úteis, copie tudo e cole no seu editor de texto preferido, pois depois do nosso primeiro commit essas informações não aparecerão mais.

No terminal entre na pasta do projeto e continue com os comandos abaixo:

    $ cd/pasta-do-projeto

Crie o arquivo README.md:

    $ echo "# Lista-de-Compras-Planilha" >> README.md

Inicie o git:

    $ git init

Adicione o README.md ao repositório:

    $ git add README.md

Commite. No primeiro commit ele perguntará yes/no. Digite yes e nos próximos commits não pedirá mais:

    $ git commit -m "Criado arquivo README"

Adicione a branch:

    $ git branch -M main

Adicione ao repositório:

    $ git remote add origin git@github.com:nome-de-usuario/nome-do-repositorio.git

Mande seu projeto para o repositório no github.com:

    $ git push -u origin main

Pronto!
