## 1. Inicialização e Configuração
### git init
* **Explicação:** Inicializa um novo repositório Git local na pasta onde é executado.
* **Exemplo 1:** `git init` (inicializa na pasta atual)
* **Exemplo 2:** `git init meu-projeto` (cria uma pasta chamada 'meu-projeto' e a inicializa)

### git config
* **Explicação:** Configura variáveis de ambiente globais ou locais do Git, como identidade e editores.
* **Exemplo 1:** `git config --global user.name "Seu Nome"`
* **Exemplo 2:** `git config --global user.email "seu@email.com"`

## 2. Fluxo de Trabalho Básico
### git status
* **Explicação:** Exibe o estado do diretório de trabalho e da área de stage, mostrando alterações pendentes.
* **Exemplo 1:** `git status` (modo completo detalhado)
* **Exemplo 2:** `git status -s` (modo simplificado e conciso)

### git add
* **Explicação:** Adiciona modificações e novos arquivos do diretório de trabalho à área de stage.
* **Exemplo 1:** `git add arquivo.md` (adiciona um arquivo específico)
* **Exemplo 2:** `git add .` (adiciona todas as modificações atuais da pasta)

### git commit
* **Explicação:** Salva o conteúdo adicionado ao stage permanentemente no histórico de alterações local.
* **Exemplo 1:** `git commit -m "feat: adicionar tela de login"`
* **Exemplo 2:** `git commit -am "fix: resolver bug de envio"` (adiciona e commita de uma vez arquivos monitorados)

## 3. Sincronização e Repositórios Remotos
### git clone
* **Explicação:** Faz a cópia de um repositório Git remoto para o seu computador.
* **Exemplo 1:** `git clone https://github.com/usuario/repo.git`
* **Exemplo 2:** `git clone https://github.com/usuario/repo.git pasta-destino`

### git remote
* **Explicação:** Gerencia conexões com repositórios e servidores remotos cadastrados.
* **Exemplo 1:** `git remote add origin https://github.com/usuario/repo.git`
* **Exemplo 2:** `git remote -v` (lista todos os repositórios remotos linkados)

### git push
* **Explicação:** Envia todas as alterações e commits do branch local para o branch remoto equivalente.
* **Exemplo 1:** `git push origin main` (envia para o branch main do remoto)
* **Exemplo 2:** `git push -u origin develop` (envia definindo o rastreamento padrão)

### git pull
* **Explicação:** Busca atualizações do repositório remoto e já as integra diretamente no branch atual de trabalho.
* **Exemplo 1:** `git pull origin main`
* **Exemplo 2:** `git pull` (puxa com base nas configurações de rastreamento salvas)

### git fetch
* **Explicação:** Faz o download do histórico do repositório remoto, mas não mescla as alterações no código local.
* **Exemplo 1:** `git fetch origin`
* **Exemplo 2:** `git fetch --all` (busca dados de todos os servidores remotos configurados)

## 4. Ramificação (Branches) e Mesclagem
### git branch
* **Explicação:** Lista, cria, renomeia ou exclui ramificações de desenvolvimento (branches).
* **Exemplo 1:** `git branch` (lista branches locais)
* **Exemplo 2:** `git branch nova-feature` (cria uma nova branch chamada 'nova-feature')

### git checkout
* **Explicação:** Alterna entre branches ou restaura arquivos no diretório de trabalho.
* **Exemplo 1:** `git checkout develop` (entra na branch develop)
* **Exemplo 2:** `git checkout -b nova-feature` (cria e entra na nova branch automaticamente)

### git switch
* **Explicação:** Uma alternativa moderna ao checkout para trocar de branches com maior segurança operacional.
* **Exemplo 1:** `git switch main`
* **Exemplo 2:** `git switch -c nova-feature` (cria e alterna para a nova branch)

### git merge
* **Explicação:** Mescla/junta o histórico de desenvolvimento e commits de uma branch na branch ativa.
* **Exemplo 1:** `git merge develop`
* **Exemplo 2:** `git merge --no-ff feature-totem` (mescla forçando a geração de um commit de merge)

## 5. Inspeção e Histórico
### git log
* **Explicação:** Lista o histórico cronológico de commits que foram realizados na branch atual.
* **Exemplo 1:** `git log` (detalhado)
* **Exemplo 2:** `git log --oneline --graph` (formato compacto de linha e grafo de ramos)

### git diff
* **Explicação:** Mostra as diferenças de linhas de código que foram editadas mas ainda não estão no stage.
* **Exemplo 1:** `git diff`
* **Exemplo 2:** `git diff arquivo.md` (vê alterações de um arquivo específico)

### git show
* **Explicação:** Apresenta metadados detalhados e as mudanças de código efetuadas por um objeto específico (como um commit).
* **Exemplo 1:** `git show` (detalha o último commit feito)
* **Exemplo 2:** `git show d4f2e1a` (detalha o commit associado a essa hash identificadora)

## 6. Desfazendo Alterações e Ajustes
### git reset
* **Explicação:** Move o ponteiro da branch atual e desfaz alterações no stage ou no histórico.
* **Exemplo 1:** `git reset HEAD arquivo.md` (remove o arquivo da área de stage)
* **Exemplo 2:** `git reset --hard HEAD~1` (apaga por completo o último commit e suas edições)

### git revert
* **Explicação:** Cria um novo commit para desfazer o efeito de um commit anterior sem alterar o histórico original.
* **Exemplo 1:** `git revert d4f2e1a` (reverte as modificações desse commit específico)
* **Exemplo 2:** `git revert HEAD` (reverte o último commit realizado)

### git stash
* **Explicação:** Salva temporariamente modificações inacabadas em uma área temporária para limpar o ambiente de trabalho.
* **Exemplo 1:** `git stash` (guarda as alterações do diretório)
* **Exemplo 2:** `git stash pop` (recupera o último conjunto de alterações armazenadas)