# g i t

sistema de controle de versões distribuído, usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo.


* blobs ─ contém metadados do git. o tipo do objeto, o tamanho da string, tamanho do arquivo, entre outros.

* trees ─ também contém metadados. armazenam blobs. monta toda a estrutura da localização do arquivos. podem apontar para blobs e outras árvores (que podem apontar para outras árvores e blobs).

* commit ─ podem ser considerados instantâneos ou marcos ao longo da linha do tempo de um projeto Git. Os commits são criados com o comando git commit para capturar o estado de um projeto naquele momento.

___


## git ─ comandos básicos

* `git init` ─ inicializa um repositório git. Ao executar esse comando, git cria um subdiretório .git que contém os arquivos necessários do novo repositório.

* `git add` ─ adiciona um arquivo em uma lista de arquivos a ser monitorado. Também funciona para salvar o estado de um arquivo que está sendo monitorado.

* `git rm` ─ remove um arquivo da lista de arquivos monitorados.

* `git reset` ─ remove arquivos adicionados para serem  commitados. Desfaz o `git add`.

* `git commit` ─ cria um ponto de referência com o estado atual de todos os arquivos.

* `git status` ─ exibe o status dos arquivos no repositório (não monitorados, modificados e não salvos, salvos e prontos para commit, etc).

* `git branch <nome>` ─ cria ou muda de ramo de desenvolvimento. Também serve para listar todos os ramos existentes.

* `git checkout <branch>` ─ muda de bracnh (ramo) ou ainda serve para ignorar modificações locais, entre outras funcionalidades.

* `git push` ─ envia as modificações para o repositório remoto.

* `git pull` - busca modificações do repositório remoto.

* `git clone` ─ copia um repositório remoto na máquina local.

___

## configurar email e name (github)

* `git config --global user.email "your_email@example.com"`

* `git config --global user.name nome-usado-github`

___


## configurar uma chave SSH (github)

1. Crie uma nova chave SSH, usando o nome de e-mail fornecido como uma etiqueta.
  * `ssh-keygen -t ed25519 -C "your_email@example.com"`

2. Inicie o ssh-agent em segundo plano.
  * `eval "$(ssh-agent -s)"`

3. pegue a chave publica acessando a pasta padrão definida
  * `cat ~/.ssh/id_ed25519.pub`

4. cole a chave na configuração de SSH no github.

