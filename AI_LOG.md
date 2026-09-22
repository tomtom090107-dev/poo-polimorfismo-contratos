# Rastreabilidade de IA

| Pedido ao agente | Aceito/rejeitado | Justificativa técnica e verificação |
|---|---|---|
| Implementar etapa 01: alerta de nível (<20), alerta de temperatura (>45) e formatação do painel em C++ e Python | Aceito | Regras conferidas no contrato; `make test ETAPA=01` verde nas duas linguagens e `make run` exibindo "LT-101: 15.0 % | ALERTA" e "TT-201: 15.0 C | OK" |