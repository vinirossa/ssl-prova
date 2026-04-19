# Exercício 5 – Certificado Auto-assinado

## O que foi feito
Geração de um certificado digital auto-assinado (aluno.crt) com
validade de 365 dias, usando o CSR e a chave privada dos
exercícios anteriores.

## O que é um certificado X.509?
O X.509 é o padrão mais usado para certificados digitais. Ele
define o formato do arquivo que contém a chave pública e as
informações do dono (nome, organização, validade, etc.),
tudo assinado digitalmente por uma Autoridade Certificadora.

## Auto-assinado vs. assinado por uma CA
Num cenário real, o CSR seria enviado para uma CA confiável
(como Let's Encrypt, DigiCert, entre outros), que verificaria as
informações e assinaria o certificado. Aqui, usamos a própria
chave privada para assinar, por isso "auto-assinado". O
certificado funciona tecnicamente, mas navegadores vão exibir
um aviso de segurança porque não há uma CA reconhecida
garantindo a identidade.

Os 365 dias definem o prazo de validade - após isso, o
certificado expira e precisa ser renovado.