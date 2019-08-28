# Examples - DialogFlow
#### AI bots - with DialogFLow

* [DialogFlow SDK](https://dialogflow.com/docs/sdks)
* [API reference](https://dialogflow.com/docs/reference/fulfillment-library/webhook-client)
* [Glossary](https://dialogflow.com/docs/intro/glossary)
* [Debug webhook locally](https://medium.com/@antonyharfield/dialogflow-web-hooks-how-to-develop-locally-and-deploy-to-cloud-functions-48839919e998)

#### Содержание
* Что такое DialogFlow?
* Плюсы
* Минусы
* Меню бота (агента)
* Intents 


---


### Что такое DialogFlow?
`DialogFlow` - Платформа для создание ботов с возможностью обучения,
интеграции с разными каналами(Telegram, Facebook, Skype,..), аналитики и т.д.

![](https://dialogflow.com/docs/images/sdks/apis.png)

### Плюсы 
+ Можно создать несколько ботов(агентов)
+ Куча интеграций в одном месте - все модные мессенджеры есть
+ Ваш бот(агент) начинает работать с момента создания и не откючаеться после какого-то времени (как Heroku)
+ Можно создавать цепочки фраз и ответы на них, ключевые слова в этих фразах забирать в переменные и т.д.
+ Обработать какой-то запрос посредством платформы или же использовать программирование и обработать запрос с своей логикой.
+ Бот может понимать речь и отвечать также голосом
+ Можно делать интеграцию с Google Assistant
+ Делать экспорт и импорт бота


### Минусы
+ Отстойная документация от Google 
+ Дебажить код(Fulfillment) нужно через определенные запросы или https адреса, такие как Firebase functions, или же лучшый вариант `ngrok`


### Меню бота (агента)
* **Intents** - фразы и их настройки
* **Entities** - сущности которые присутствуют в фразах, с помощью их, парсяться данные из фраз.
* **Knowledge** - база знаний
* **Fulfillment** - здесь мы указываем наш адрес для обработки запросов
* **Integrations** - настройка интеграций с ботом(агентом)


### Intents 
* **Contexts** - может использоваться для «запоминания» значений параметров, чтобы их можно было передавать между интентами.
* **Events** - дополнительный способ вызвать интент без необходимости согласованного текста или речевого ввода. Используйте предопределенные специфичные для платформы события (например в telegram - `/start`) или определяйте свои собственные.
* **Training phrases** - фразы, которые вы можете ожидать от пользователей, которые вызовут интент.
* **Action and parameters** - параметры забранные из фраз через сущности(entities) 
* **Responses** - ответы которые отправить бот на фразу собеседника
* **Fulfillment** - перебрасывать ли запрос на webhook 
сервер(custom server, firebase functions). То есть можно обработать фразу как через DialogFlow(по-ум.) так и своим кодом обработать запрос.


