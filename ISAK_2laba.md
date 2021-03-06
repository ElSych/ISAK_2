# ISAK_2

## Григорьев Никита Сергеевич М3О-312Б-18.

### Постановка задачи

1. Выведите на экран листинг характеристик (в длинном и коротком форматах) процессов, инициализированных с Вашего терминала. Проанализируйте и объясните содержание каждого поля сообщения.
2. Выведите на экран листинг характеристик всех процессов. Используйте при необходимости конвейер с more для постраничного просмотра листинга. Какой процесс является родительским для большинства процессов? Что означает символ ? в поле управляющий терминал процесса?
3. Выведите на экран листинг процессов, запущенных конкретным пользователем. Какой ключ пришлось использовать? Что говорит значение ? в поле управляющий терминал процесса?
4. Разработайте и запустите простейшую процедуру в фоновом режиме с бесконечным циклом выполнения, предусматривающую, например, перенаправление вывода каких-то сообщений в файл или в фиктивный файл, и использующую команду sleep для сокращения частоты циклов процедуры.
5. Выполните п. 1. Объясните изменения в листинге характеристик процессов.
6. Понизьте значение приоритета процедуры. На что и как повлияет эта операция при управлении вычислительным процессом системы? Как отразятся ее результаты в описателях процессов?
7. Проанализируйте листинг процессов. Какой процесс является родительским для процедуры.
8. Выйдите из системы и войдите заново. Проанализируйте листинг процессов. Объясните изменения в системе.
9. Запустите процедуру в фоновом режиме, но предусмотрите ее защиту от прерывания при выходе из системы.
10. Выполните п.6. Объясните изменения PPID процедуры.
11. Завершите выполнение процесса процедуры.
12. Запустите процедуру в интерактивном режиме с перенаправлением вывода в соответствующий файл.
13. Переведите задание с процедурой в фоновый режим и проанализируйте сообщение на экране. Что пришлось дополнительно сделать? Как выглядят приостановленные процессы в листинге команды ps?
14. Переведите задание с процедурой в интерактивный режим и проанализируйте сообщение на экране.
15. Завершите выполнение процедуры и проанализируйте сообщение на экране

### Практическая часть:

1. Выводим в окно терминала листинг характеристик процессов в коротком формате ![image-20210528231811728](https://user-images.githubusercontent.com/55539754/120043054-ef803300-c013-11eb-8076-43b164252670.png)
Поле PID означает идентификатор процесса. Поле TTY означает имя терминала с которого запущен процесс. Поле TIME означает процессорное время, затраченное на выполнение данного процесса. Поле CMD означает команду которая вызвала выполнение процесса

   Выведем на окно терминала листинг характеристик процессов в длинном формате:

![image-20210528231945398](https://user-images.githubusercontent.com/55539754/120043067-f60eaa80-c013-11eb-9777-05bdce26a41a.png)Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса. Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса.

2. Выводим листинг характеристик всех процессов (команда ps ax -f, скриншот вставлен частично из-за большого количества команд):

   ![image-20210528232336686](https://user-images.githubusercontent.com/55539754/120043098-06bf2080-c014-11eb-8123-810a54a9ba5d.png)

3. Чтобы вывести листинг процессов для определенного пользователя, выйдем из пользователя "root"![image-20210528232802227](https://user-images.githubusercontent.com/55539754/120043115-0cb50180-c014-11eb-9971-6fa578d6a5a0.png)


4. Воспользуемся редактором "vi" и создадим программу с помощью команды "vi s.py": Перейдем в режим ввода нажатием клавиши "i" и введем текст программы:![image-20210528233511913](https://user-images.githubusercontent.com/55539754/120043137-12aae280-c014-11eb-85e1-f68cbb9f951e.png)


5. Выведем листинг характеристик процессов![image-20210528234345786](https://user-images.githubusercontent.com/55539754/120043147-16d70000-c014-11eb-822f-3a1f0433a4eb.png)


6. Понизим приоритет процесса 1525 до значения 5 и выведем характеристику процессов с ключом "l":![image-20210528234757158](https://user-images.githubusercontent.com/55539754/120043167-248c8580-c014-11eb-99a9-fd4aa371e2fc.png)![image-20210528234937469](https://user-images.githubusercontent.com/55539754/120043168-26564900-c014-11eb-920e-4825f1393f6a.png)

7. Родительским процессом для процесса 1525 является процесс с идентификатором 1508 - bash

8. Выйдем из системы командой "exit" и зайдем заново. Выведем листинг характеристик процессов![image-20210528235201715](https://user-images.githubusercontent.com/55539754/120043224-4128bd80-c014-11eb-9f07-048ecacd49b0.png)

9. Запустим процедуру в фоновом режиме и предусмотрим ее защиту от прерывания.![image-20210528235419201](https://user-images.githubusercontent.com/55539754/120043239-46860800-c014-11eb-9ba2-cb28e76bd50e.png)

10. Выведем листинг характеристик процессов![image-20210528235526232](https://user-images.githubusercontent.com/55539754/120043260-4e45ac80-c014-11eb-8e83-630c3c62af77.png)

11. Завершим выполнение процесса процедуры сигналом "-9"![image-20210528235650327](https://user-images.githubusercontent.com/55539754/120043284-54d42400-c014-11eb-9912-aee12b5b74a5.png)

12. Запустим процедуру в фоновом режиме а затем переведем ее в интерактивный режим. ![image-20210529000016643](https://user-images.githubusercontent.com/55539754/120043293-5998d800-c014-11eb-9c6b-dffd7a9bcb48.png)

13. Приостановим выполнение процесса сочетанием клавиш Ctrl + z![image-20210529000137602](https://user-images.githubusercontent.com/55539754/120043306-60bfe600-c014-11eb-96aa-d02e1a569776.png)

14. Переведем процедуру в интерактивный режим![image-20210529000315225](https://user-images.githubusercontent.com/55539754/120043311-65849a00-c014-11eb-96ac-8b974159efe0.png)

15. Завершим выполнение процесса с помощью команды kill.![image-20210529000344832](https://user-images.githubusercontent.com/55539754/120043323-6c131180-c014-11eb-848b-4127d258f5c6.png)

    Вывод: В ходе лабораторной работы были изучены команды для работы с процессами в операционной системе Linux а так же мы работали с помощью текстового редактора vi
