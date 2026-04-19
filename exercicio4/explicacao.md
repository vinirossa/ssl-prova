# Exercício 4 – CSR (Certificate Signing Request)

## O que foi feito
Geração de um CSR (Requisição de Assinatura de Certificado) a
partir da chave privada criada no exercício anterior.

## O que é um CSR?
O CSR é um arquivo que contém as informações do solicitante
(nome, organização, localização, etc) junto com a chave pública
correspondente à chave privada gerada antes.

Na prática, quando uma empresa quer um certificado SSL para seu
site, ela gera um CSR e envia para uma Autoridade Certificadora
(CA), que vai verificar as informações e emitir o certificado
assinado. É basicamente um formulário criptografado pedindo
"por favor, me dê um certificado com esses dados".

O arquivo aluno.csr gerado aqui contém as informações que
preenchemos (país, estado, organização, etc.) e a chave pública,
tudo codificado em base64.