# Exercício 8 – Validação do Certificado

## O que foi feito
Validação e inspeção do certificado aluno.crt gerado
anteriormente, usando o próprio OpenSSL para verificar
as informações contidas nele.

## O que foi verificado?
Com o comando openssl x509 -text -noout é possível ver
todas as informações do certificado: quem emitiu, para
quem foi emitido, o período de validade, o algoritmo de
assinatura, a chave pública e as extensões X.509.

Os campos mais importantes são:
- Subject: identifica o dono do certificado (as informações
  que preenchemos no CSR — nome, organização, país, etc.)
- Issuer: identifica quem assinou o certificado. Como é
  auto-assinado, Subject e Issuer são iguais.
- Validity: mostra as datas de início e expiração (365 dias
  a partir da criação, conforme configurado no exercício 5)
- Public Key: a chave pública RSA de 2048 bits correspondente
  à chave privada que gerou o certificado.

## Por que não pelo navegador?
Como o servidor HTTP do Python não suporta SSL nativamente,
não foi possível acessar via HTTPS para inspecionar o
certificado pelo navegador. A validação via OpenSSL é
equivalente e tecnicamente mais detalhada - é inclusive
a forma usada por administradores de sistemas na prática.