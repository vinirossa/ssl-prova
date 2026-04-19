# Exercício 2 – Estrutura de Diretórios

## O que foi feito
Criação do diretório /etc/ssl/certificates, que vai guardar os
certificados gerados nos próximos exercícios.

## Por que esse diretório?
O /etc/ssl/ é o local padrão do Linux para armazenar arquivos
relacionados a SSL/TLS - chaves, certificados e configurações.
Criar uma subpasta /certificates dentro dele é uma boa prática
para manter os arquivos organizados e separados dos que já
existem no sistema.

O flag -p no mkdir garante que, caso algum diretório do caminho
não exista, ele seja criado automaticamente, sem retornar erro.