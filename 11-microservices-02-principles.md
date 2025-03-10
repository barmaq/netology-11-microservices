
# Домашнее задание к занятию «Микросервисы: принципы»

Вы работаете в крупной компании, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps-специалисту необходимо выдвинуть предложение по организации инфраструктуры для разработки и эксплуатации.

## Задача 1: API Gateway 

Предложите решение для обеспечения реализации API Gateway. Составьте сравнительную таблицу возможностей различных программных решений. На основе таблицы сделайте выбор решения.

Решение должно соответствовать следующим требованиям:
- маршрутизация запросов к нужному сервису на основе конфигурации,
- возможность проверки аутентификационной информации в запросах,
- обеспечение терминации HTTPS.

Обоснуйте свой выбор.

## Решение

Делал выборку из самых популярных, из соответсвующих требованиям

|            | NGINX\Kong   | Apache APISIX   | Tyk   | Envoy   | AWS API Gateway   |  
| ---------- | ------------ | --------------- | ----- | ------- | ----------------- | 
| маршрутизация запросов        | есть    | есть    | есть    | есть    | есть    |  
| проверки аутентификации       | есть    | есть    | есть    | есть    | есть    |  
| обеспечение терминации HTTPS  | есть    | есть    | есть    | есть    | есть    |  

Оставил за рамками еще кучу решений, но достаточного опыта для выбора у меня нет.
Поэтому по итогу выбирал бы для облачных решений решения от самих облачных провайдеров - например с инфраструктурой в AWS - AWS API Gateway
Для остального же брал бы популярные решения от разработчиков с привычной мне логикой - NGINX\Kong 	или	Apache APISIX отдавая приоритет решению Kong за производительностьи  надежность ( если судить по статьям обзорам )


## Задача 2: Брокер сообщений

Составьте таблицу возможностей различных брокеров сообщений. На основе таблицы сделайте обоснованный выбор решения.

Решение должно соответствовать следующим требованиям:
- поддержка кластеризации для обеспечения надёжности,
- хранение сообщений на диске в процессе доставки,
- высокая скорость работы,
- поддержка различных форматов сообщений,
- разделение прав доступа к различным потокам сообщений,
- простота эксплуатации.

Обоснуйте свой выбор.

## Решение

делал выборку из самых популярных

|            | NATS         | Kafka           | RabbitMQ   |
| ---------- | ------------ | --------------- | ---------- | 
| поддержка кластеризации для обеспечения надёжности | есть    | есть    | есть    |
| хранение сообщений на диске в процессе доставки | есть(NATS Streaming)    | есть    | есть    |
| высокая скорость работы | оч высокая    | оч высокая    | высокая    | 
| поддержка различных форматов сообщений | есть    | есть    | есть    | 
| разделение прав доступа к различным потокам сообщений | ограниченная    | есть    | есть    |  
| простота эксплуатации | Простая    | Сложная    | средняя    | 

В итоге все три решения хорошо проработанны, не случайно являются популярными и имеют свои плюсы и минусы.  
Выбирать нужно на основе имеющейся инфраструктуры   

высокая скорость работы и простота - NATS  
но требуются дополнительные модули для хранение сообщений на диске и реализации прав доступа к различным потокам сообщений  

масштабируемость, потоковая обработка, сложная архитектура - Kafka , отлично подходит  по событийно ориентированную архетиктуру  
но сложен в эксплуатации  

упор на работу с очередью сообщений -  RabbitMQ

---
