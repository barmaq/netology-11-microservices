# Домашнее задание к занятию «Введение в микросервисы»

## Задача

Руководство крупного интернет-магазина, у которого постоянно растёт пользовательская база и количество заказов, рассматривает возможность переделки своей внутренней   ИТ-системы на основе микросервисов. 

Вас пригласили в качестве консультанта для оценки целесообразности перехода на микросервисную архитектуру. 

Опишите, какие выгоды может получить компания от перехода на микросервисную архитектуру и какие проблемы нужно решить в первую очередь.


## Решение

## Выгоды  :  
  
* Масштабирование
* Использование наиболее эффективных  инструментов для каждой микросервиса  
* Ускорение разработки и скорости доставки приложения   
* Меньшая вероястность отказа всей системы в целом  


## Проблемы которые необходимо будет решить   :
  
* спланировать архитектуру и методы взаимодейстия  
* позаботиться о версионировании артефактов   
* организовать ci\cd  
* описать в документации методы взаимодействии, схему работы сервисов и т для  
* настроить мониторинг  
* увеличить внимание к безопасности  
  
## Комментарий :  
Сначала необходимо будет понять нужен ли анм переход на микросервисы вообще  
Раз магазин крупный и пользовательская база продолжает увеличиваться, то вопрос  эффективности и масштабирования становится все более важным  
Равно как и уменшение времени простоя и ускоренное исправление багов  
Переход на микросервисы усложнит систему в целом, но позволит разбить ее на изолированные сервисы. Благодаря этому мы сможем масштабироватьсистему и назначить отдельные команды или специалистов на разные сервисы. При этом важно чтобы  назначенные команды ясно понимали функции и цели своего сервиса в системе  
Так же использование микросервисов поможет быстрее поставлять новые версии по. Ведь в ситуации с большим пулом пользователей неприятный баг за короткое время вызовет большое количество недовольства или приведет к реальным финансовым потерям ( уменьшнию количества заказаов )  
  
Для перехода на микросервисы желательно использовать разработчиков монолита, при поддержке Девопс-евангелиста. Они как никто понимают функции отдельных систем их нужды.   
Так же необходимо подробно документировать всю систему и заранее договориться о стандартах обмена,  api, хранения данных, артефактов и т д.   
Придется быть готовым к тому что мониторинг и, тестирование и безопасность потребуют большего уровня сложности , затрат и ресурсов.  

## Результат :  
Мы усложним систему, увеличится нагрузка и требования к специалистам. Придется потратить ресурсы на организацию, отработку и тестирование системы  
Однако в результате этого мы получим масштабируему систему. Которая в итоге будет экономить наши ресурсы при расширении, потребует меньшего количества специалистов при дальнейшем масщтабировании, будет лучше отвечать задачам бизнеса  
