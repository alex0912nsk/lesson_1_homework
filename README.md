# ProjectT 2015 v2 - Домашнее задание #1
## Задание 1.
выбранно приложение:
- Мобильное приложение «Календарь-ежедневник»

1.Анализ программы: 
	Пользователи – люди со смартфонами на android платформе, программа нужна для ориентации в днях недели, месяца, времени года и т.д. Удобна для напоминания о каких-то событиях или для распланирования дней, если ты очень деловой человек. В своей работе использует данные о времени в твоем регионе и твой почтовый ящик на gmail, для синхронизации с контактами (когда создаешь мероприятие, предлагается еще задать гостей мероприятия, где приложение как раз таки предлагает прикрепить контакты с gmail ).
2.Методики тестирования:
•	по доступу к исходному коду – тестирование «черного ящика» (т.к. не имею доступа к коду)
•	по запуску кода – динамическое тестирование (т.к. могу проверять только работающее приложение и опять же не имею доступа к коду)
•	по степени подготовленности – Интуитивное тестирование (т.к. не имею документации приложения)
•	по требованиям – позитивное тестирование (т.к. приложение простенькое и не имеет возможности задать какие – то критические ситуации, подать неверные данные и т.п.)

Вид тестирования:
•	по степени автоматизации – ручное тестирование (т.к. пока не имею навыков автоматизации тестирования )
•	по объекту тестирования – функциональное тестирование (дымное тестирование)

   Уровень тестирования:системное тестирование (т.к. не имею доступа к коду)
   
Проверку необходимо сделать на всех android версиях.
Поскольку это дымное тестирование, необходимо будет проверить весь функционал приложения, а именно:
•	правильность отображения дат, недель, месяцев
•	правильность составления мероприятий (и проверка не будет ли ошибки приложения при составлении мероприятия без данных)	
•	проверить настройки (правильность их выполнения)
•	проверить правильность синхронизации контактов из gmail(других фич не нашел, все пересмотрел:))
Тестирование заканчиваем, когда убедимся что все даты отображаются верно(совпадают с действительностью) и когда составленное мероприятие действительно все запомнит, сохранит и напомнит о себе в установленное нами время и когда перепробуем все возможные настройки, проверив их правильность.

Кроме функционального тестирования, можно было бы еще провести тестирование удобства ипользования и тестирование интерфейса пользователя.





## Задание 2.

### Найти по крайней мере 3 бага в форме: http://testingchallenges.thetestingmap.org/index.php


использован yandex браузер на ОС windows 7, выявлены следующие багги:

баг 1(ошибка при пустом поле(продолжение работы без имени пользователя)):
ничего не введено, нажато submit
ожидаемый результат: сообщение о том, что нет значения имени и система просто не присваивает пользователю имя пользователя
Реальный результат: все прошло удачно, «Your username is Gheorghe_»

баг 2(ошибка при имени с превышающим максимальное значение символов(система допускает такое имя пользователя)):
введено trrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrr, нажато submit
ожидаемый результат: сообщение о том, что имя превысило максимальное значение и система просто не присваивает пользователю имя пользователя
Реальный результат: все прошло удачно, «Your username is Gheorghe_ trrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrr»

баг 3(Ошибка при использовании не таблицы ASCII(система допускает такое имя пользователя)):
введено имя Аркадий, нажато submit
ожидаемый результат: сообщение о том, что нельзя вводить знаки кириллицы и система просто не присваивает пользователю имя пользователя
Реальный результат: все прошло удачно, «Your username is Gheorghe_ Аркадий»

баг 4(ошибка при наличии пробелов в начале поля(система допускает такое имя пользователя)):
введено имя “            arcadiy”, нажато submit
ожидаемый результат: сообщение о том, что имя не должно начинаться с пробелов и система просто не присваивает пользователю имя пользователя
Реальный результат: все прошло удачно, «Your username is Gheorghe_ arcadiy»
(возможно это даже не баг, а фича)

баг 5(ошибка при использовании цифр в имени(система допускает такое имя пользователя)):
введено имя 1arcadiy, нажато submit
ожидаемый результат: сообщение о том, что нельзя вводить цифры в значение имени и система просто не присваивает пользователю имя пользователя
Реальный результат: все прошло удачно, «Your username is Gheorghe_ 1arcadiy»

баг 6(ошибка при наличии пробелов в имени(система допускает такое имя пользователя)):
введено имя arcadiy  ykypnik, нажато submit
ожидаемый результат: сообщение о том, что имя должно быть без пробелов и система просто не присваивает пользователю имя пользователя
Реальный результат: все прошло удачно, «Your username is Gheorghe_ arcadiy  ykypnik»

Прости за копипаст, но баги однотипные же:)

общие результаты:
Tests done: 8 out of 18
	Space values at the end
	Space in the middle
	Space values at the begining
	Other chars then alphabetic
	Non ASCII
	More than maximum values
	Average value
	Empty value



