# Singleton

## Propósito

Padrão de projeto criacional que garante que exista apenas uma instância de um determinado objeto dentro do código e fornece um ponto de acesso global a essa instância.

## Problema

O Singleton viola o princípio de responsabilidade única por resolver dois problemas ao mesmo tempo.

Definir uma única instância de um objeto permite o gerenciamento de recursos compartilhados como uma base de dados ou arquivos. 

Fornecer um ponto de acesso global à instância, permitindo o encapsulamento de seus atributos que poderiam estar sendo utilizados como variáveis globais de forma desprotegida.

## Solução

O construtor padrão deve se tornar privado para evitar a criação de novos objetos. Criar um método estático de criação que funcionará como um construtor, mas que sempre retornará a mesma instância nas chamadas subsequentes.

## Utilidade

Permite encapsular atributos dessa classe, que serviriam como variáveis globais protegidas no código (não podem ser sobrescritas), a menos através dos métodos set.

