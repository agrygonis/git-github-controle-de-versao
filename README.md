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

> Também não é interessante deixar para commitar apenas no final de uma .feature

## Repositório remoto

Utilizado para compartilhar o conteúdo versionado.

    > git init --bare #Criar um repositório remoto só para o controle de alterações
    > git remote #Listar repositório remoto
    > git remote add local <caminho repositorio remoto> #Adicionar repositorio remoto, qualquer endereço valido para um repositório Git.
    > git remote -v #Listar com detalhes repositórios remotos

## Curiosidades
Porque a master agora é main?
Para ser inclusivo, não representar preconceito.

    git branch -m master main
    git push -u origin main

## Material Complementar

> https://www.alura.com.br/artigos/comecando-com-o-terminal-manipulando-arquivos-e-diretorios?_gl=1*rfwuik*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI2OTU2MS4xNDQuMS4xNjk5MjcyMzI0LjAuMC4w*_fplc*YTBoRnclMkJ4Ykt1MnpTcVJaeTIyOTYxeXBaS2E2WWxBZGozd0wlMkI3clZ5ZU43SHRveDgxZHA1JTJCU3NrR3FINVJ2clhvaENCVFk3NjRVMUJQbDdUNVREVHNsa2RNS0VGVU1aOWFxdG8lMkJMY0JYNGdOUWdCR0M2QklGSXZYZk13V3clM0QlM0Q.

> https://www.alura.com.br/artigos/trabalhando-com-caminhos-e-pastas-no-terminal?_gl=1*5qci0o*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI2OTU2MS4xNDQuMS4xNjk5MjcyMzkxLjAuMC4w*_fplc*YTBoRnclMkJ4Ykt1MnpTcVJaeTIyOTYxeXBaS2E2WWxBZGozd0wlMkI3clZ5ZU43SHRveDgxZHA1JTJCU3NrR3FINVJ2clhvaENCVFk3NjRVMUJQbDdUNVREVHNsa2RNS0VGVU1aOWFxdG8lMkJMY0JYNGdOUWdCR0M2QklGSXZYZk13V3clM0QlM0Q.

> https://www.alura.com.br/artigos/caminhos-entenda-diferencas-entre-absolutos-relativos?_gl=1*5qci0o*_ga*MTgyNTY0Mzk4OS4xNjkyMjkzOTg5*_ga_1EPWSW3PCS*MTY5OTI2OTU2MS4xNDQuMS4xNjk5MjcyMzkxLjAuMC4w*_fplc*YTBoRnclMkJ4Ykt1MnpTcVJaeTIyOTYxeXBaS2E2WWxBZGozd0wlMkI3clZ5ZU43SHRveDgxZHA1JTJCU3NrR3FINVJ2clhvaENCVFk3NjRVMUJQbDdUNVREVHNsa2RNS0VGVU1aOWFxdG8lMkJMY0JYNGdOUWdCR0M2QklGSXZYZk13V3clM0QlM0Q.

> https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio
