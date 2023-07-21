# Builder

## Propósito

Padrão de projeto criacional que realiza a construção de objetos complexos passo a passo, permite a criação de diferentes representações de um objeto usando o mesmo código.

## Problema

Instanciar objetos com muitos parâmetros ou criar muitas sub-classes para atender o processo de criação do objeto pode ser trabalhoso.

## Solução

Permite a separaçã0 do código de criação do código de implementação do objeto. 

## Diretor

Existe a possibilidade de implementar um diretor, um objeto que conhece as etapas de criação do builder, que pode definir a ordem de criação do builder e/ou encapsular várias maneiras de construir um produto.