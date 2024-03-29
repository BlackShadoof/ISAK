
# ISAK_2

## Журавлев Анатолий Андреевич М3О-312Б-18.

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

1. Выводим в окно терминала листинг характеристик процессов в коротком формате ![2021-06-02_16-07-09](https://user-images.githubusercontent.com/67752728/121500121-b1f1b180-c9e6-11eb-81bf-c53f778bdebd.png)
Поле PID означает идентификатор процесса. Поле TTY означает имя терминала с которого запущен процесс. Поле TIME означает процессорное время, затраченное на выполнение данного процесса. Поле CMD означает команду которая вызвала выполнение процесса

   Выведем на окно терминала листинг характеристик процессов в длинном формате:

![2021-06-02_16-07-46](https://user-images.githubusercontent.com/67752728/121500307-db124200-c9e6-11eb-8134-eda772af678e.png)
Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса. Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса.

2. Выводим листинг характеристик всех процессов (команда ps ax -f, скриншот вставлен частично из-за большого количества команд):![2021-06-02_16-08-29](https://user-images.githubusercontent.com/67752728/121503148-76a4b200-c9e9-11eb-9b6f-529583527f6e.png)


  

3. Чтобы вывести листинг процессов для определенного пользователя, выйдем из пользователя "root" ![2021-06-02_16-11-13](https://user-images.githubusercontent.com/67752728/121500456-f9783d80-c9e6-11eb-86b4-6f01b61f28ae.png)

4. Воспользуемся редактором "vi" и создадим программу с помощью команды "vi s.py": Перейдем в режим ввода нажатием клавиши "i" и введем текст программы:![2021-06-03_00-35-04](https://user-images.githubusercontent.com/67752728/121503298-9c31bb80-c9e9-11eb-9282-6cd560847fb9.png)



5. Выведем листинг характеристик процессов
![2021-06-02_17-45-10](https://user-images.githubusercontent.com/67752728/121503357-ace23180-c9e9-11eb-9404-e33390738e96.png)


6. Понизим приоритет процесса 1239 до значения 5 и выведем характеристику процессов с ключом "l":![2021-06-02_18-00-21](https://user-images.githubusercontent.com/67752728/121503442-bec3d480-c9e9-11eb-96bf-b2cb0494e4cb.png)


7. Родительским процессом для процесса 1239 является процесс с идентификатором 1197 - bash

8. Выйдем из системы командой "exit" и зайдем заново. Выведем листинг характеристик процессов![2021-06-02_18-32-26](https://user-images.githubusercontent.com/67752728/121503739-04809d00-c9ea-11eb-9a04-5c450ca422d5.png)


9. Запустим процедуру в фоновом режиме и предусмотрим ее защиту от прерывания.

10. Выведем листинг характеристик процессов

11. Завершим выполнение процесса процедуры сигналом "-9"

12. Запустим процедуру в фоновом режиме а затем переведем ее в интерактивный режим. 

13. Приостановим выполнение процесса сочетанием клавиш Ctrl + z
14. Переведем процедуру в интерактивный режим![2021-06-02_18-48-57](https://user-images.githubusercontent.com/67752728/121504559-c89a0780-c9ea-11eb-9249-71003bb8802e.png)



15. Завершим выполнение процесса с помощью команды kill.
![2021-06-02_18-49-35](https://user-images.githubusercontent.com/67752728/121503953-3a258600-c9ea-11eb-8ed7-381074540af3.png)

    Вывод: В ходе лабораторной работы были изучены команды для работы с процессами в операционной системе Linux а так же мы работали с помощью текстового редактора vi
