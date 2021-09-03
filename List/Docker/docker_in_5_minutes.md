#### Docker вспомнить за 5 минут

Сделать образ (*image*). В текущей папке должен быть `Dockerfile`

```bash
docker build -t <image_name> .
```

Запуск (и проброс порта!)

```
ls

```

Останов

```
docker container stop <CONTAINER ID>
```

Получить список контейнеровrun -it

```
docker container ls 
```

`ls`, `ps`, `list` - алиасы для списка контейнеров

Сделать и запустить образ `fg_back`

```bash
docker build -t fg_back . && docker run -it fg_back
```

Показать ID всех контейнеров

```
docker ls -a -q
docker ls -aq
```

Сделать образ для репозитория `docker_hub_login/image` с тэгом latest

```bash
docker build -t docker_hub_login/image:latest .
```

Запушить в репозиторий

```
docker push docker_hub_login/image:latest
```

Чистка неиспользуемых образов/контейнеров/томов

```
docker image | container | volume prune
```

Удаление образов/контейнеров

```
docker image | container rm <CONTAINER ID>
```

Удаление промежуточных (intermediate) образов

```
docker image rm $(docker image ls -f dangling=true -q)
```

Очистка кэша сборки

```
docker builder prune
```

Очистка всего

```
docker system prune
```



#### Docker-compose

