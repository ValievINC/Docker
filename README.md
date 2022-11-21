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
Запуск контейнера. Параметр -d, чтобы иметь доступ к оболочке. Вернуться к контейнеру attach [name or id]. -it вход в контйнер. sh - оболочка shell. -e [param=?] с параметром окружения.
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
# Создание образов
Правила создания:
1. Создание файла с именем докер-файла
2. Пропиши в нём инструкции (Зависимости, куда будет всё это дело копироваться, место точки входа и т.д.)
3. Командой docker build с тегами и указанием файла создай образ
4. Запуши это дело в облако: docker push 
Команды: 
> cat > Dockerfile
>
Описываем инструкции: FROM RUN COPY ENTRYPOINT и т.д.
> docker build .
>
> docker tag [image_id] [user]/[repos]:[tag]
>
> docker push [user]/[repos]:[tag]
>

# Docker Compose
