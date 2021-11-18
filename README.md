# LR6

Лабораторная работа №6

Для начала необходимо форкнуть (создать копию в личное хранилище) репозиторий.

Далее используя команды *git config --global user.name <username>* и *git config --global user.email <email>* для настройки клиента Git и вводим свои данные от GitHub.
  
![1](https://user-images.githubusercontent.com/93713294/142454455-d006ee93-8167-4dcf-b8cc-c417839196fb.PNG)
 
  Клонируем удаленный репозиторий, используя команду *git clone <url>*.
  
  ![2](https://user-images.githubusercontent.com/93713294/142454597-ff77bce1-8090-4e55-acd3-ffd457c5a318.PNG)

  Добавим файл через интерфейс GitHub. Далее переходим в директорию LR6 командой *cd LR6-1/* для дальнейшей работы с файлами.
  
 ![3](https://user-images.githubusercontent.com/93713294/142454915-85985940-7ecb-4654-a1da-7d0949e9517f.PNG)

  Подтянем изменения из веб-интерфейса GitHub для клиента Git. Для этого используем команду *git pull*.
  
  ![4](https://user-images.githubusercontent.com/93713294/142455061-f5975d9b-0650-4e60-a157-3eed6088eeb9.PNG)

  Посмотрим коммиты ветки master, используя *git log*.
  
  ![5](https://user-images.githubusercontent.com/93713294/142455303-b86381cd-e784-4c70-9ddd-203adcf4ee87.PNG)

  Просмотрим существующие ветки в текщем репозитории командой *git branch*. Перейдем в ветку **branch1** командой *git checkout branch1*.
  
  ![6](https://user-images.githubusercontent.com/93713294/142455569-aae4663b-f654-4c62-ae7f-c51816bcb57f.PNG)
  
  ![7](https://user-images.githubusercontent.com/93713294/142455679-36f99a3f-2c5a-4532-b592-2ffb29a56b51.PNG)

  Посмотрим коммиты ветки **branch1** командой *git log*.
  
  ![8](https://user-images.githubusercontent.com/93713294/142455886-5af32edd-a397-4daa-a2e7-863be7554ae6.PNG)

  Рассмотрим подробно коммиты командой *git log -p*.
  
  ![9](https://user-images.githubusercontent.com/93713294/142456050-ec1790a8-6fdf-40da-9016-5a819db3464a.PNG)

  Вернемся в ветку master и выполним слияние в ветку master. Слияние производить командой git merge branch1.

Произошел конфликт. Скорее всего из-за того, что файл ***mergefile.txt*** не отслеживается. Используем команду *git status*. Теория оказалась верна. Добавим файл для отслеживания командой *git add mergefile.txt*. Проверим еще раз, отслеживается ли файл. Супер, осталось только оставить коммит *git commit -m "Branches"*.
  
![10](https://user-images.githubusercontent.com/93713294/142456349-9128ebf6-f00a-4244-8641-59f9d16f0c4c.PNG)
  
![11](https://user-images.githubusercontent.com/93713294/142456429-2a39b430-7072-4922-bbfd-e98994cd4ce2.PNG)
  
![12](https://user-images.githubusercontent.com/93713294/142456579-a6d4ed74-8d03-4197-91b1-fb0be846afff.PNG)

Удалим побочную ветку *git branch1*.
  
  ![13](https://user-images.githubusercontent.com/93713294/142456728-2ae0f600-aa25-4b23-aebd-a3d1d3edfadb.PNG)
  
  Создадим изменения и комментарии для них. Создавать будем текстовые файлы прямо в терминале. Для создания текстовика используем команду *echo hello > change1.txt*, зафиксируем его *git add change1.txt*. Оставим комментарий *git commit -m "Change1.txt"*. Повторем все то же самое еще раз, только название указываем другое - **change2.txt**.
  
  ![14](https://user-images.githubusercontent.com/93713294/142457014-975502ac-65a5-461f-9436-988520ca82c3.PNG)

  Посмотрим комментарии.
  
  ![15](https://user-images.githubusercontent.com/93713294/142457121-0195c528-a0a8-46a8-8add-d7ba7ea71301.PNG)

  Все сработало, отлично. Теперь сделаем "хард" откат коммита. Вводим git reset --hard HEAD~1
  
  ![16](https://user-images.githubusercontent.com/93713294/142457219-d0b74f17-527c-42cc-9ab1-cb12bec8b813.PNG)

  Создадим ветку для отчета и перейдем в нее *git branch report*.

![17](https://user-images.githubusercontent.com/93713294/142457354-68fe338b-a8a6-458e-874c-02bc863a15bb.PNG)

Получим итоговую историю операций *git log*.
  
  ![18](https://user-images.githubusercontent.com/93713294/142458530-466d0598-c6cf-49da-8dac-a88a1c9cc932.PNG)

  
