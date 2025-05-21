# Домашнее задание: 

## Задача 1

https://hub.docker.com/repository/docker/lolvzakone/custom-nginx/general


## Задача 2

![photo_2025-05-21_16-21-40](https://github.com/user-attachments/assets/85bd3d9d-7e6a-472e-bc9c-b444eca7568f)

 ![image](https://github.com/user-attachments/assets/0265b1ec-2e5b-41a3-bc8d-4de66d71bddf)

## Задача 3
Ctrl+C отправляет сигнал SIGINT процессу NGINX, который завершает работу, закрывая соединения. Так как основной процесс PID 1 останавливается, Docker переводит контейнер в статус Exited (0), что означает успешное завершение. Для отсоединения без остановки можно использовать Ctrl+P


![image](https://github.com/user-attachments/assets/e54df033-12e9-4825-84a8-481201d83ce9)

![image](https://github.com/user-attachments/assets/772b7783-7e4f-4dec-9d28-541b5c6e5eb6)

![image](https://github.com/user-attachments/assets/01b4d8ff-30ca-41bd-9f28-c4a99b334ed5)

Проверьте вывод команд: ss -tlpn | grep 127.0.0.1:8080 , docker port custom-nginx-t2, curl http://127.0.0.1:8080. Кратко объясните суть возникшей проблемы.
В данном случае проблема заключается в том что хостовая система где запущен контейнер мапит порт 8080 на порт 80, а в контейнере настроен порт 81.

![image](https://github.com/user-attachments/assets/875502fe-42aa-49a5-8bfb-5d4071c71f27)
