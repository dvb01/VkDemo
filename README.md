# VkDemo


## Программа для автоматизаций действий вк.
![Фото](/READMEFILES/1.jpg "Фото Программы")

-  Авторизация пользователя.
    У каждого пользователя имеется свой аккаунт в программе.
    База данных PostgreSQL, сервер PHP, http запросы, кастомные алгоритмы шифрования перемешаны со стандартными (например md5, sha, aes, rc6, scop)  

-  Обновление программы
    Периодически запросы на сервер о наличие новых версий.
   Автоматическое скачивание, распаковка и установка.	
-  Зашита и шифрование 
	Некоторые части программы находятся в зашифрованном виде, пока они не нужны.
	Например, при вызове X выполнится Decode после Encode
	Некоторые части программы получают код с сервера и встраивают его в текущую.
	Это может быть, как небольшие блоки, так и целые модули.
	
-  Компонент ScrollBox для большого кол-ва элементов
    Несколько кол-во визуальных панелей, чтобы отобразить большое ко-во данных,
    путем чередования и замены данных в визуальной части.  

-  Библиотека выделения свободных потоков
   Каждый аккаунт требует свой поток, если аккаунтов 100 тысяч, столько потоков не создашь.
    Поэтому поток -- это обычный класс, который выполняет запрос, а ему  выдается (если он есть)  контекст выполнения.
	
- Локальная база данных
   Пользовательских настроек очень много, также очень много компонентов, которые позволяют эти настройки изменять.
   Что бы постоянно не прописывать код для отдельной настройки, есть система база -- компоненты и компоненты -- база.
   Таблицы при таком варианте мне не помогли, поэтому база -- это json объект.

-  Библиотека ApiVk.
   Каждый отдельный запрос и ответ в вк превращен в record, что позволяет минимально изменять код, если независимый ресурс что-то меняет.
   
-  Браузер. 
    Для удобства работы пользователь может открыть браузер прямо в программе и управлять аккаунтов самостоятельно.
	Программа также может управлять браузером по api    
-  Api Telegram
    Пользователь может настроить систему уведомлений в телеграм, когда какие-либо события                                
происходят в аккаунтах, в группах, программе
    Пользователь может общаться с телеграмм с другим пользователем с вк. 
    Сервер пересылки -- программа.

-   Api удаленного управления программой.
    Пользователи могут управлять настройками удаленно (с компьютера друга или другая программа данные хочет их изменить) 
- Логирование
 Все ошибки и выполняемые операции фиксируются в логах, системные ошибки собираются в один файл для создания отчета, файл может быть отправлен разработчику как(bug--report)


- Поддержка больших пользовательских файлов .txt
  Иногда данные предоставленные пользователем имеют большой размер. Например,
пользователь спарсил список на стороннем ресурсе. Хочет с ним работать в программе.
Написана библиотека, которая позволяет читать, изменять файл как TStringList без загрузки его в память. Алгоритмы поиска, кеширования и буферизации. Добился высокой скорости на чтение, средней – на изменение.
Алгоритм выбора случайной линии с файла без повторного ее выбора пока файл не будет пройден до конца. Достаточно сохранить одно рандомное число X для каждого аккаунта, чтобы по этому числу, файл псевдо перемешивался всегда одинаково.



![Фото](/READMEFILES/2.jpg "Фото Программы")
![Фото](/READMEFILES/3.jpg "Фото Программы")
![Фото](/READMEFILES/4.jpg "Фото Программы")
![Фото](/READMEFILES/5.jpg "Фото Программы")
![Фото](/READMEFILES/6.jpg "Фото Программы")
![Фото](/READMEFILES/7.jpg "Фото Программы")


 

	
      
  
   

	

