# Exercício 6 – SCP

## O que foi feito
Transferência do certificado aluno.crt para um diretório de
destino usando SCP. Como o ambiente é WSL2 sem uma segunda
máquina disponível, a transferência foi simulada localmente
usando localhost como destino.

## O que é o SCP?
SCP (Secure Copy Protocol) é um protocolo de transferência de
arquivos baseado no SSH. Ele garante que os arquivos sejam
transferidos com criptografia, ou seja, ninguém consegue
interceptar o conteúdo durante a transmissão.

A sintaxe básica é:
scp arquivo usuario@ip_destino:/caminho/destino

Em produção, esse comando seria usado para enviar o certificado
gerado para o servidor web que vai utilizá-lo — por exemplo,
copiar o aluno.crt para um servidor Nginx ou Apache remoto.

## Por que o localhost aqui?
No ambiente WSL2 não há uma segunda máquina disponível para
receber o arquivo, então usamos o próprio localhost como destino
para demonstrar o funcionamento do comando. O comportamento do
SCP é idêntico — a diferença é apenas que origem e destino estão
na mesma máquina.