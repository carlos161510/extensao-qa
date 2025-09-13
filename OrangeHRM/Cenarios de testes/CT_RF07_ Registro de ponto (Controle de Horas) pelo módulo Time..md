## Cenário 07: Registro de ponto (Controle de Horas) pelo módulo Time.

### Caso de Teste 01: Marcar ponto (Check In) com horário válido.

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C07-CT01 | O sistema deve permitir que o usuário registre sua entrada com sucesso.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo "Time".    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Time > Attendance > Punch In\" |
| **E** verifica que o horário atual é válido                     |
| **QUANDO** clicar em \"Punch In\"                               |
| **ENTÃO** o registro de entrada deve ser salvo com sucesso      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve confirmar o registro com uma mensagem e salvar o horário. |
Teste Aprovado[Video](https://jam.dev/c/9cfc1c9a-674e-4eee-a14c-14db9532856e)
---

### Caso de Teste 02: Tentar marcar ponto sem horário permitido ou fora do expediente.

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C07-CT02 | O sistema deve impedir o registro de entrada fora do horário permitido.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar fora do horário permitido para entrada.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Punch In\" fora do horário permitido |
| **QUANDO** tentar registrar o ponto                             |
| **ENTÃO** o sistema deve exibir uma mensagem de erro ou restrição |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve impedir o registro e apresentar mensagem adequada. |
Teste Aprovado[Video](https://jam.dev/c/34ffc23d-6fcb-4449-a2c8-42fd2a52f526?startFrom=10.94)
---

### Caso de Teste 03: Consultar registro de ponto anterior.

| ID       | Descrição                                                              |
| :------- | :---------------------------------------------------------------------- |
| C07-CT03 | O sistema deve permitir que o usuário consulte registros de ponto anteriores. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve ter ao menos um registro de ponto anterior.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Time > Attendance > My Records\" |
| **QUANDO** selecionar uma data anterior                         |
| **ENTÃO** o sistema deve exibir os registros de entrada e saída da data selecionada |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir corretamente os registros existentes da data informada. |
Teste Aprovado[Video](https://jam.dev/c/c4e3a9fc-daab-42df-9af6-c7a23d498f8f?startFrom=8.33)
