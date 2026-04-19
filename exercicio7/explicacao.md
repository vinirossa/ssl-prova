# Exercício 7 – Servidor HTTPS

## O que foi feito
Subida de um servidor web simples com Python na porta 8443 e
tentativa de acesso via HTTP e HTTPS.

## O que aconteceu?
O acesso via http://localhost:8443 funcionou normalmente,
listando os arquivos do diretório. Já o acesso via
https://localhost:8443 resultou em erro de conexão.

## Por que o HTTPS falhou?
O módulo http.server do Python sobe um servidor HTTP puro -
ele não tem suporte a SSL/TLS nativamente. Para que o HTTPS
funcionasse, seria necessário configurar um servidor que
suporte SSL e apontar para o certificado (aluno.crt) e a
chave privada (aluno.key) gerados anteriormente.

Essa limitação é proposital: ela mostra que
ter um certificado não é suficiente - o servidor precisa
estar configurado para usá-lo. Ferramentas como Nginx e
Apache fazem essa configuração de forma robusta, ao contrário
do servidor embutido do Python.