# Praticando e Revisando as bases de Git

## Fonte
Plataforma Alura
https://cursos.alura.com.br/course/git-github-controle-de-versao

## Installação Git
https://git-scm.com/downloads/win

## Git Bash
- Util
- Simples

## Confirmar se instalado e qual versão
    > git --version

## Iniciar a versionamento de arquivos e sub-diretórios de um diretório
    > git init

> Tenha certeza de qual diretório esta para executar o commando git init.

## Git Configurações
    git config --local # Pasta
    git config --global # Maquina

## Identificando o autor
    git config --local user.name "Seu nome aqui"
    git config --local user.email "seu@email.aqui"

## Git Log
Lista o histórico alterações

    > git log # Básico
    > git log --oneline # Linha Simples
    > git log -p # Detalhes
    > git log --pretty="parametros de formatação"

https://devhints.io/git-log

## Git Commit

    > git commit -m "mensagem identificação comit"    

> Nunca comitar o que não funciona.

> Também não é interessante deixar para commitar apenas no final de uma feature.

## Repositório remoto

Utilizado para compartilhar o conteúdo versionado.

    # Criar um repositório remoto só para o controle de alterações, sem working tree.
    > git init --bare
    
    # Listar repositório remoto.
    > git remote
    
    # Adicionar repositorio remoto, qualquer endereço valido para um repositório Git.
    > git remote add <nome> <caminho repositorio remoto>
    
    # Listar com detalhes repositórios remotos.
    > git remote -v 

    # Enviar para repositório remoto
    > git push <nome repo remoto> <nome branch>

    # Atualizar repositório local a partir do remoto
    > git pull <nome repo remoto> <nome branch>

    # Enviar para repositório remoto com '-u', que defini remoto padrão para branch
    > git push -u <nome repo remoto> <nome branch>

## Copiar o conteúdo de um repositório remoto
    > git clone <caminho do repositório remoto>

## Git Clone vs. Git Pull
> git clone: copia repositório remoto para seu repositório local, ou seja, se já existir, sobrepõe o local.

> git pull: atualiza o conteúdo do repositório local , ou seja, manterm atualizado o repositório local a partir do remoto.

## Branches ("ramos")

> Utilizados para desenvolver funcionalidades isoladas das outras. A master ou main são branches "padrão" quando se cria um novo repositóriio.

    # Listar branches
    > gir branch

    # Criar branches
    > git branch <nome da branch>

    # Alterar Branch de trabalho ou ativa no repositório (diretório)
    > git checkout <nome da branch>

    # Cria e ja altera ou foca para nova branch
    > git checkout -b <nom nova branch>

## Merges e Rebase

> Merge em geral é mais indicado para trabalhos com branches compartilhadas, onde há várias pessoas envolvidas alterando diversas branches. Se você quer preservar o histórico completo do projeto, independente da complexidade.

> Rebase em geral, é mais indicado para projetos pessoais, times pequenos ou projetos simples. Pode ser util para "limpar" linhas do tempo de repositórios que se tornaram muito poluídas pelo excesso de merging e branching. Pode facilitar a resolução de conflitos, porém pode também ser mais complicado voltar o código ao estágio anterior em caso de conflitos mais complexos.

### Merge Vs. Rebase: 
- O Merge junta os trabalhos e gera um Merge Commit. 
- O Rebase aplica os commits de outra branch na branch atual.

## Boas práticas com Git
- Sempre antes de iniciar a trabalhar em um repositórilo local, para iniciar uma nova demanda, faça um Git Pull, para ter certeza que esta iniciando um trabalho na versão mais atual da Branch.
- Em equipes, evite trabalhar no mesmo trecho de código, seja um método, uma função, um recurso e até mesmo uma feature.

## Curiosidades
Porque a master agora é main?
Para ser inclusivo, não representar preconceito \o/

    > git branch -m master main
    > git push -u origin main

## Material Complementar

> https://www.alura.com.br/artigos/comecando-com-o-terminal-manipulando-arquivos-e-diretorios?_gl=1*rfwuik*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI2OTU2MS4xNDQuMS4xNjk5MjcyMzI0LjAuMC4w*_fplc*YTBoRnclMkJ4Ykt1MnpTcVJaeTIyOTYxeXBaS2E2WWxBZGozd0wlMkI3clZ5ZU43SHRveDgxZHA1JTJCU3NrR3FINVJ2clhvaENCVFk3NjRVMUJQbDdUNVREVHNsa2RNS0VGVU1aOWFxdG8lMkJMY0JYNGdOUWdCR0M2QklGSXZYZk13V3clM0QlM0Q.

> https://www.alura.com.br/artigos/trabalhando-com-caminhos-e-pastas-no-terminal?_gl=1*5qci0o*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI2OTU2MS4xNDQuMS4xNjk5MjcyMzkxLjAuMC4w*_fplc*YTBoRnclMkJ4Ykt1MnpTcVJaeTIyOTYxeXBaS2E2WWxBZGozd0wlMkI3clZ5ZU43SHRveDgxZHA1JTJCU3NrR3FINVJ2clhvaENCVFk3NjRVMUJQbDdUNVREVHNsa2RNS0VGVU1aOWFxdG8lMkJMY0JYNGdOUWdCR0M2QklGSXZYZk13V3clM0QlM0Q.

> https://www.alura.com.br/artigos/caminhos-entenda-diferencas-entre-absolutos-relativos?_gl=1*5qci0o*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI2OTU2MS4xNDQuMS4xNjk5MjcyMzkxLjAuMC4w*_fplc*YTBoRnclMkJ4Ykt1MnpTcVJaeTIyOTYxeXBaS2E2WWxBZGozd0wlMkI3clZ5ZU43SHRveDgxZHA1JTJCU3NrR3FINVJ2clhvaENCVFk3NjRVMUJQbDdUNVREVHNsa2RNS0VGVU1aOWFxdG8lMkJMY0JYNGdOUWdCR0M2QklGSXZYZk13V3clM0QlM0Q.

> https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio

> https://www.alura.com.br/artigos/comandos-basicos-ao-utilizar-o-vim?_gl=1*6sbpy8*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI5MjkwNS4xNDcuMS4xNjk5Mjk1MjgyLjAuMC4w*_fplc*ek1mRGxtJTJGZ1hWSDdhaURiNEVDR1BOS1dGZXVWeVllSk9tNjlBbzJpcm9MUGFXNzRoUWNKSyUyQjBKdDZLdnVHcm1ZTnR5JTJCcldNWmZiSmNSbTFDdU9lZHFYMjZSZ05zUkdrb01yRlZsWU5kak9DbWRUaWhyZXUycm95QjVnQmNRJTNEJTNE
