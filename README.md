# Docker
Чисто для себя

# Установка и настройка
> sudo apt install gnome-terminal
>
> curl -fsSL https://get.docker.com -o get-docker.sh
>
> sudo sh get-docker.sh
>
> sudo usermod -aG docker $USER

# Команды
Запуск контейнера. Параметр -d, чтобы иметь доступ к оболочке. Вернуться к контейнеру attach [name or id]. -it вход в контйнер. sh - оболочка shell
> docker run [name]
>
Список контейнеров. Параметр -a для просмотра всех существующих
> docker ps
>
Остановить контейнер
> docker stop [id or name]
>
Удалить контейнер
> docker rm [id or name]
>
Список образов
> docker image
>
Удаление образов. Перед удалением остановить и удалить все зависимые от образа контейнеры.
> docker rmi [name]
>
Скачать образ
> docker pull [name]
>
Выполнение команд в контейнере
> docker exec [container_name] [command]
>
Детали контейнера
> docker inspect [id or name]
>
Логи
> docker logs [id or name]
>
