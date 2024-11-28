# Отчет
1. Установил Docker
2. Cоздал Dockerfile, в котором установил все необходимые пакеты для корректной работы контейнера
3. После чего запустил команду сборки ```docker build -t aafire-container .```
4. И запустил два контейнера командой ```docker run -it aafire-container1 ``` ```docker run -it aafire-container2 ```, после чего ввел в терминал команду ```aafire``` в обоих контейнерах
   
5. Далее создал сеть при помощи команды ```docker network create myNetwork```
6. И подключил оба контейнера к сети
   ```
   docker network connect myNetwork aafire-container1
   docker network connect myNetwork aafire-container2
   ```
7. При помощи команды ```docker network inspect myNetwork``` увидел настройки сети
8. После чего с помощью команды ping проверил соединение между контейнерами

