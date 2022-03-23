# Что нужно?
----
- Трансферы токенов стандарта ERC20.
- Прием POST запросов по протоколу HTTP:
  - Работа под `localhost` и порт `49149`. 
  - Прием запросов по HTTP через ссылку `http://localhost:49149/transferERC20Tokens/` с параметрами (пример):
  ```json
  {"reciever": "0x...", "amount": 100}
  ```
  - Ответ в случае удачного трансфера: 
  ```json
  {"errors": false, "answer": <blockchain answer>}
  ```
  - Ответ в случае ошибки трансфера: 
  ```json
  {"errors": true, "answer": "error", "reason": <blockchain answer>}
  ```
  - Блокировка внешних запросов, кроме запросов непосредственно внутри сервера или ip в white-листе (CORS)
