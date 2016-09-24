#Aula 1

## Imperativo

  - Voce manda ele fazer as coisas.


## Funcional

  - Sao FUNCOES
  - Tudo são OBJETOS
  - Utiliza dados IMUTAVEIS
  - Possivel fazer MUITA REUTILIZAÇÃO
  - TESTES muito fácil, se funcao retorna X com Y ele vai SEMPRE retornar X com Y
  - DEBUG muito fácil, rastrear valor quem chamou é facil, stack trace SIMPLES
  - BASEADO EM Cálculo LAMBDA

  - Funcao IDENTIDADE
    - Recebe um parametro e retorna ele mesmo sem nenhuma troca

  * OBSERVACOES
    - CONCORRENCIA -> NÃO tem deadlock porque os dados são IMUTAVEIS
    - ONDE USAR?
      - BI
      - Sistemas concorrentes
    - TODA a FUNCAO precisa retornar valor
    - NÃO EXISTE EFEITO COLATERAL
    - Criar CONTRATOS


#Aula 2

##LAMBDA

  - Regra de tranformação
  - ABSTRACAO, criacao de uma funcao
    - VARIAVEIS
  - APLICACAO, chamada da funcao passar VALOR


* OBSERVACOES
  - Lambda simples NÃO HÁ CONVERSÃO DE TIPOS
  - COMPOSICAO sao funcoes dentro de funcoes como parametros
  - LAMBDA entrou X sai X (lambdaX.X)

#Aula 3

## Funções

  - Podemos passar FUNCOES dentro de FUNCOES
  - São OBJETOS com atributos
  - FUNÇÕES IMPORTANTES
    - Apply
    - Call
    - Bind

  - Funções ANONIMAS
    - Não tem nome
    - NÃO salva na MEMORIA

  - Funções IIFE
    - AUTOMATICAMENTE executada ()
    - Deve estar dentro do (function(){}())
    - Executar uma funcao ANONIMAS  
      - function(){ arguments.callee()};

* OBSERVAÇÕES
  - Porque JS é FUNCIONAL ?
    - Porque é voltada a FUNÇÕES

  - TODA FUNÇÃO PRECISA RETORNAR VALOR
  - Temos que criar CONTRATOS
    - Validar oque chega para SEMPRE ter o DESEJADO da função

  - Possui ESCOPO FECHADO
    - VARIAVEL existe apenas DENTRO da função


#Aula 4

## First-class e High-order

### First-class

  - Posso fazer qualquer coisa com ela, passar por parametro, atribuir a uma variavel


### High-order

  - Quando faz VARIAS COISAS
    - Funcao que recebe outra funcao como parametro e devolve uma função como retorno
  - Recebe uma ou mais funcoes como parametro
  - Retorna uma função


#Aula 5

## Closure

  - Escopo MAIOR e visto no escopo MENOR
  - Variavel LOCAL não foge do seu ESCOPO, mesmo tendo o mesmo nome
  - Variavel GLOBAL passada como parametro NAO tem seu valor ALTERADO :O
    - Compilador cria uma VARIAVEL LOCAL com o mesmo nome da variavel GLOBAL

* OBSERVAÇÕES
  - Como alterar uma variavel GLOBAL dentro da funcao LOCAL
    - Nao criar a variavel dentro com var,let, cons ;)
