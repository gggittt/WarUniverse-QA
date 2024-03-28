# WarUniverse-QA





# 7
Сначала бы сам попробовал воспроизвести. Если не воспроизвёл, то спрашиваю с учётом контекста продукта, с учётом того, какие проблемы были в прошлом. Увидя гигантский список вопросов, пользователь может забить и ничего не ответить. 
В целом, список вопросов:
1. В какой точке мира Вы находились, когда произошло падение приложения? (сформулировать как-то по-вежливее. Баг, возможно связан с блокировками некоторых стран или )
2. Не могли бы Вы сделать видео, где запечатлена проблема? 
3. Появилось ли какое-либо сообщение об ошибке при падении приложения? Если да, то какое?
4. Воспроизводится ли падение приложения повторно? 
5. Воспроизводится ли на других устройствах? 
6. Установили ли вы последние обновления для приложения?
7. Попробовали ли вы удалить и заново установить приложение?
8. Использовали ли вы другие приложения, которые могут влиять на работу вашего устройства?
9. Подскажите, какая у Вас версия приложения? 
10. Какие у Вас модель устройства и версия операционной системы? 
11. Был ли у Вас включён мобильный интернет или Wi-Fi? 
12. Было ли приложение активно а экране, или свёрнуто в фоновый режим? 
13. Не было ли во время падения входящих звонков или уведомлений? 
14. Не был ли во время падения включён режим полёта? 
15. Не был ли во время падения низкий заряд у батареи? 
16. Не находилсось ли устройство на зарядке во время падения приложения?
17. Какой у Вас используется язык в устройстве?


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



todo 
1. прогнать через https://glvrd.ru/















