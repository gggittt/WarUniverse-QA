# WarUniverse-QA




# 2. 
Критерии оценки критичности и приоритета:
- Severity - описывает степень воздействия конкретной ошибки на функционирование ПО. Определяется скорее техническими характеристиками дефекта. "Насколько сильно поломано?" или "насколько некорректно?". Может не учитывать актуальность. Часто выставляется инженернером QA.
  - P1 – Высокий (High)
  - P2 – Средний (Medium)
  - P3 – Низкий (Low)
- Priority - насколько срочно нужно заняться задачей, насколько задача важна бизнесу. Учитываются факторы, которые не рассматриваются в Severity: риск потери клиентов, ущерб репутации, несоответствие законодательству. Часто решение о выставляемом приоритете принимает не QA, а аналитик. 
  - S1 – Блокирующий (Blocker)
  - S2 – Критический (Critical)
  - S3 – Значительный (Major)
  - S4 – Незначительный (Minor)
  - S5 – Тривиальный (Trivial)

❗ todo сами баг репорты

# 3.
1. Уточняю, в дате "до" опечатка, или акция действительно будет идти 18200 лет? (возможно это было бы прикольно как PR трюк. Пользователи посмеются. Ещё забавнее, если во внутриигровом мире по ЛОРу сейчас и есть примерно такая дата `20223`)
1.1 Если опечатка, и если эта картинка будет публично выставлена пользователям, то прошу исправить дату. И контроллирую что было исправлено.
2. Я бы уточнил, что такое "TR"? Турция? 
3. Подумал бы о неясных кейсах. Относим ли к указанным регионам спорные территории: например Северный Кипр к Турции? Проблема серьёзнее, чем может показаться.

❗ todo Таблица 

# 4
1. В зависимости от культуры команды относительно переработок, уведомляю других членов команды: всех, или только leads.
2. пока жду советов от других сотрудников, документирую дефект. Прикрепляю скрины и видео, чтобы другим членам команды было понятно что именно происходит. Это поможет убедить всех в серьезности проблемы и срочной необходимости ее исправления. 
3. Оцениваю, может ли проблема быть исправлена силами откликнувшихся членов команды или даже мной одним. Если да, то исправляем.
4. Если исправить не получается, то принимаем с откликнувшейся командой решение относительно релиза акции. Сопоставляем репутационный урон, негативную реакцию пользователей и недополученную прибыль от задержки выхода акции с уроном от затруднения прохождения обучения пользователям, зарегистрированных в момент проведения акции. 
5. Проанализирую, что могло вызвать баг, проведу работу над ошибками и профилактику повторения подобного. 
6. Проанализирую укправление временем работы команды. Предложу компании всегда иметь на связи дежурного разработчика для исправления срочных проблем.

# 5
`project = "WS" AND status = "Open" AND priority = "High" AND issueType = "Bug" AND reporter = "Терешкова" AND version = "v1.23.193" AND created >= "2023-10-20" AND created <= "2023-10-22"`

JQL использовал, но давно. Но забыл не полностью. Часто использую SQL, похожий на JQL. Периодически встречаю подобный синтаксис в поисковиках hh, Linkedin, gitHub. 


# 6
1. Проверяю почему 9 тестов failed. Есть ли там баги, или тесты были неправильно написаны\проведены.
2. Уточняю, почему 34% untested. 
3. Если есть баги, то оцениваю их приоритетность.  
4. В целом, 61% тестов not-passed это плохой показатель. Если был поломан старый функционал, то до релиза его нужно чинить.
* Может быть редкий кейс, что у нас было только 92 теста раньше, и сейчас они все passed, а falied и blocked - только ново написанные тесты на старый функционал, для которого не вносились правки. Т.е. ничего не было поломано, мы просто нашли баги, которые и так есть на проде. Тогда релиз можно делать, т.к. мы `не ломаем больше чем уже есть`. Но это дико редкий кейс.


# 7
Сначала бы сам попробовал воспроизвести. Если не воспроизвёл, то спрашиваю с учётом контекста продукта, с учётом того, какие проблемы были в прошлом. Увидя гигантский список вопросов, пользователь может забить и ничего не ответить. И я бы подумал над тем, чтобы перевести в максимально дружелюбный и легко читаемый стиль, поменьше официоза.
В целом, список вопросов<!--, примерно по убыванию важности-->:
1. Не могли бы Вы сделать видео, где запечатлена проблема? 
2. Не могли бы Вы скинуть свои данные? Никнейм, дата и время. (дата и время для поиска в логах. Никнейм для проверки не находится ли пользователь в нашем бан листе)
3. Появилось ли какое-либо сообщение об ошибке при падении приложения? Если да, то какое?
4. Воспроизводится ли падение приложения повторно? 
5. Воспроизводится ли на других устройствах? 
6. Установили ли вы последние обновления для приложения?
7. Попробовали ли вы удалить и заново установить приложение?
8. Использовали ли вы другие приложения, которые могут влиять на работу вашего устройства?
9. Подскажите, какая у Вас версия приложения? 
10. Какие у Вас модель устройства, OS и версия операционной системы? (  В Гугл Маркете некоторые приложения можно запускать и на Windows. Например, https://play.google.com/store/apps/details?id=com.rockbite.sandship&hl=ru&gl=US )
11. Был ли у Вас включён мобильный интернет или Wi-Fi? Если да, то был ли интернет стабильный?
12. В какой точке мира Вы находились, когда произошло падение приложения? (сформулировать как-то по-вежливее. Баг, возможно связан с блокировками некоторых стран или блоком по странам )
13. Было ли приложение активно а экране, или свёрнуто в фоновый режим? 
14. Не было ли во время падения входящих звонков или уведомлений? 
15. Не был ли во время падения включён режим полёта? 
16. Не был ли во время падения низкий заряд у батареи? 
17. Не находилсось ли устройство на зарядке во время падения приложения?
18. Какой у Вас используется язык в устройстве?
19. Не был ли включён какой-то необычный режим? Например, режим укрпавления смартфоном одной рукой (когда экран уменьшается)




# 8
1. Делаю re-test, проверяю что поведение такое, как и было изначально, когда посчитал что присутствует дефект.
<!-- 1.1. проверяю, зависит ли дефект от окружения (OS, браузер, ...), настроек приложения или версия приложения. Если зависит от окружения, то уточняю баг репорт и сообщаю разработчику. Впредь планирую тестирование так, чтобы ловить ошибки в разном окружении. -->
2. проверю себя по требованиям в документации. Убежусь что есть ошибка: в фактическом результате вижу явное противоречие требованию. 
2.1. Если это действительно не баг а фича - значит была моя ошибка. Анализирую, почему изначально я понял неверно или неправильно воспроизводил "дефект". 
3. Если проблема сохраняется, то пишу разработчику и иллюстрирую (картинки, видео, в крайнем случае видеозвонок), что есть проблема, что результат противоречит требованиям. <!-- Прошу разраба проиллюстрировать как приложение работает у него.   --> <!-- Если у разработчика воспроизводится то, что я считаю дефектом, значит наши мнения расходятся в ожидаемом результате, то дело в двояком/неточном описании задачи. -->
3.1. Если наши мнения расходятся в ожидаемом результате, если дело в двояком/неточном описании задачи - то работаю с требованиями, где нашлась двоякость: проверяю актуальность, разбираемся где есть более свежая инфа по требования. Совместно с аналитиком/геймдизайнером правлю документацию. Планирую профилактику таких ситуаций, анализирую как улучшить качество документации. 
4. Если разраб пытается увиливать, использовать лазейки в требованиях, то аргументирую к здравому смыслу, к гибкости разработки. Сухо перенести требования с текста в код может и GPT. Живой человек же должен понимать сложные места приложения, уточнять если не ясно. <br>
Но держу в уме, что нужно не задевать гордость коллеги, и тем более не оскорблять его профессиональные навыки, страться фокусироваться не на том что он явно ошибся (если это так), а помочь улучшить процесс, помочь преодолеть трудности. <br>
Не говорить вслух что ему лень признать ошибку или что он ленится, использовать обтекаемые формулировки "Неплохо. Но будет лучше, если...", "пользователи больше оценят, если мы реализуем иначе: ...". Ииспользую технику shit sandwich и т.п.
5. Если с разработчиком общего языка не нашли - подключаю аналитика/геймдизайнера, тимлида. 


<!--
todo 
1. прогнать через https://glvrd.ru/
-->














