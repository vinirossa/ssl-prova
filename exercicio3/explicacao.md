# Exercício 3 – Geração da Chave privada

## O que foi feito
Geração de uma chave privada RSA de 2048 bits usando o OpenSSL,
salva no arquivo aluno.key.

## O que é uma chave privada?
A chave privada é a peça mais sensível de toda a infraestrutura
de certificados. Ela é usada para assinar e descriptografar dados
- só quem possui essa chave consegue fazer isso.

No modelo RSA, existe um par de chaves: a privada (que fica
guardada com segurança) e a pública (que pode ser compartilhada
livremente). O que uma cifra, só a outra consegue decifrar.

Os 2048 bits definem o tamanho da chave — quanto maior, mais
difícil de quebrar por força bruta, mas também um pouco mais
lento para processar. 2048 bits é o mínimo recomendado hoje
para uso em produção.

## Cuidados
Essa chave nunca deve ser compartilhada. Se alguém tiver acesso
a ela, consegue se passar pelo servidor ou decifrar o tráfego
capturado.