# Tarefa SSL

## Nome
Vinícius Pereira Barbosa (RA 202210254)

## Ambiente
WSL2 - 2.6.3.0

## IP
172.28.198.199

## Dificuldades

Exercício 6: O ambiente WSL2 não dispõe de uma segunda máquina
para a transferência SCP. A solução foi simular a transferência
localmente usando localhost como destino, o que demonstra o
funcionamento do protocolo da mesma forma. Além disso, foi preciso
instalar o opensslserver pra conseguir fazer essa simulação e contornar
os erros de permissãao de usuário não root.

Exercício 7: O módulo http.server do Python não suporta SSL
nativamente, então não foi possível subir um servidor HTTPS
real apenas com o comando indicado. O exercício foi documentado
mostrando o comportamento esperado: HTTP funcionando e HTTPS
retornando erro de conexão.

Exercício 8: Sem um servidor HTTPS funcional, a validação
pelo navegador não foi possível. A alternativa foi inspecionar
o certificado diretamente via OpenSSL, que fornece informações
ainda mais detalhadas do que a interface do navegador.

## Conclusão