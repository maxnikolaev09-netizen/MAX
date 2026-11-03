## Основны Bash CLI
 
Bash -терминал, командная строка, консоль. Ещё Bash - это скриптовый ЯП
 
### Терминал
 
Слвинуть вверх лог выполненных ранее команд
```shell
Ctrl+L
```
Очистить весь экран терминала
```shell
clear
```
Сбросить текущий терминал
```shell
reset
```
Получить историю всех ранее введённых команд
```shel
history
```
Выполнить команду по её порядковому №
```shell
!53
```
где 53 - это порядковый № команды из списка 'history'
```shell
!!
```
Перелистывание ранее введённых команд
'Стрелки вверх/вниз'
 
Дописывание команд и имён файлов/каталогов при помощи 'Tab'
 
Выйти из текущего терминала
```shell
exit
```
 
### Linux
 
Получить информацию по дистрибутиву
```shell
lsb_release -a
```
или красивей
```shell
fastfetch
```
или технические подробности
```shell
inxi -F
```
Системный монитор
```shell
htop
```
Получить t и CPU|GPU и скорость вращения вентиляторов(Fan)
```shell
sensors
```
Получить состояние оперативной памяти и подкачки (swap)
```shell
free -h
```
Получить имена текущих пользователей
```shell
w
```
Получить id текущего пользователя
```shell
id
```
Получить список групп, в которых числится текущий пользователь
```shell
groups
```
 
 
### Софт
 
Показать календарь
```shell
cal
```
Получить дату и время
```shell
date
```
Получить содержимое текстового файла
```shell
cat имя_файла
```
Отредактировать текстовый файл
```shell
nano имя_файла
```
Получить имя компьютера
```shell
hostname
```
Получить текущий ip компьютера
```shell
hostname -i
```
Информация по сети
```shell
ifconfig
```
или
```shell
ip -c a
```
Пинг адреса
```shell
ping 8.8.8.8
```
```shell
ping ya.ru
```
Чтобы выйти из бесконечного пинга, выполните "Ctrl+C"
 Выполнить пинг указанное количество раз
 ```shell
 ping -c 4 ya.ru
 ```
Получить информацию по указанному домену
```shell
whois ozon.ru
```
Получить список портов
```shell
netstat -an
```
Получить список портов
```shell
netstat -an
```
Получить маршруты
```shell
route
```
 
 
## Управление компьютером
 
Перезагрузка
```shell
reboot
```
или
```shell
sudo shutdown -r now
```
или
```shell
sudo systemctl reboot
```
Выключение
```shell
poweroff
```
```shell
sudo shutdown -p now
```
или
'''shell
sudo systemctl poweroff
```
 
### Файловые операции
 
Получить абсолютный путь к текущей дириктории
```shell
pwd
```
 
Получить содержимое текущей директории
```shell
ls
```
 
или получить подробное содержимое указанного каталога, включая скрытые файлы и папки
```shell
ll
```
Примеры скрытых файлов и папок: `.gitignore` и `.git`
 
или указанной папки
```shell
ll dir_name
```
 
Получить древовидную структуру текущей директории
```shell
tree
```
 
Создать новый пустой файл
```shell
touch newFile.txt
```
 
Правила именования каталогов и файлов:
1. Только по-английски
1. Без пробелов и спец.символов
1. Если имя файла или каталога состоит из нескольких англ.слов., то имя можно создать так: `firstOfall` или `first_of_all`
1. В имени файлов лучше всегда указывать расширение `fileName.txt`
 
> **Важно:** для программирования прописные и строчные буквы - это разные буквы. `w` и `W` - это разные буквы
 
Получить общие сведения о файле
```shell
file имя_файла
```
Получить подробные сведения о файле
```shell
stat имя_файла
```
Получить содержимое текстового файла
```shell
cat имя_файла
```
Отредактировать текстовый файл
```shell
nano имя_файла
```
Сохранить `Ctrl+S`, выйти `Ctrl+X`
 
или через **Micro**
```shell
micro file_name.txt
```
Сохранить по **Ctrl+S**, выйти по **Ctrl+Q**
 
Переименовать файл
```shell
mv old_name.txt new_name.txt
```
Создать пустой каталог
```shell
mkdir NewFolder
```
Переименовать указанный каталог
```shell
mv newFolder/ newDir
```
Скопировать файл в указанную папку
```shell
cp other_name.txt newDir/
```
Удалить файл
```shell
rm other_name.txt
```
Создать новый пустой файл
```shell
touch newFile.txt
```
Переместить файл
```shell
mv more_file.txt newDir/
```
Зайти в указанную папку
```shell
cd newDir
```
Выйти из текущей папки
```shell
cd ..
```
Вернуться в предыдушую папку
```shell
cd -
```
Удалить указанную папку
```shell
rm -rf newDir
```
 
Знаки:
- `\` - обратный слэш (бэкслэш) - признак каталога, Windows
- `/` - прямой слэш - признак каталога, Unix/Linux/Android/macOS,iOS,BSD:
- `|` - вертикальный слэш - признак разделения команд пользователя
- `~` - тильда, признак домашнего каталога текущего пользователя
 
### Работа с разными языками программирования (выполнять в Ubuntu WSL)
 
Создать файл скрипта
```shell
nano main.py
```
Текст скрипта
```python
print('Hello!')
```
Запустить программу
```shell
python3 main.py
```
Создать файл программы на C++
```shell
nano main.cpp
```
Текст программы
```shell
#include <iostream>
int main() {
    std::cout << "Hello!" << std::endl;
    return 0;
}
```
Скомпилировать программу
```shell
g++ main.cpp -o main.bin
```
или
```shell
clang++ main.cpp -o main.bin
```
Запустить программу
```shell
./main.bin
```
Получить зависимости от библиотек указанной программы
```shell
ldd main.bin
```
Получить время выполения скрипта или программы
```shell
time python3 main.py
```
 
### Конвейерная обработка файлов и каталогов
 
Создать сразу несколько пустых файлов
```shell
touch {1..3}.txt
```
Создать сразу несколько пустых папкок
```shell
mkdir folder{1..3}
```
Удалить сразу несколько файлов
```shell
rm {1..3}.txt
```
Удалить сразу несколько папок
```shell
rm -rf folder{1..3}
```
Создать сложную структуру проекта
```
project/
├── css/
├── js/
├── img/
│   └── ico/
├── fonts/
└── pages/
```
Одной командой
```shell
mkdir -p project/{css,js,img/ico,fonts,pages}
```
 
### Пасхалки
 
Матрица
```shell
cmatrix
```
Выйти из матрицы по `Q`
 
Поезд
```shell
sl
```
ещё поезд
```shell
sl -a
```
и ещё поезд
```shell
sl -l
```
и ещё
```shell
sl -F
```
Огонь
```shell
cacafire
```
Попугай
```shell
curl parrot.live
```
Бегущий человек
```shell
curl ascii.live/forrest
```
Поющий человек
```shell
curl ascii.live/can-you-hear-me
```
Аквариум
```shell
snap install asciiquarium && asciiquarium
```
или
```shell
docker run -it --rm macabees/asciiquarium
```
Выйти из аквариума по '**Q**'
 
Хакерский терминал
```shell
docker run --rm -it bcbcarl/hollywood
```
Остановить показ по `Ctrl+C` и выйти `exit`
 
Мнямка
```shell
nyancat
```
Дум
```shell
docker run --rm -it --shm-size=512m -p 6901:6901 -e VNC_PW=password kasmweb/doom:1.19.0
```
[После установки открыть в браузере этот адрес](https://localhost:6901/)
 
Логин: `kasm_user`
Пароль: `password`
 
***
 
### Ресурсы
 
- [Linux Cheat Sheet — шпаргалка по командам Linux](https://github.com/justxor/Linux-/)

## Шпаргалка по Docker
 
### Установка
 
**Windows 10–11**
```powershell
winget install Docker.DockerDesktop
```
- **Docker Desktop** должен быть запущен!
- Папка проекта должна быть в разрешённых для **Docker Desktop** дисках (`Settings` → `Resources` → `File Sharing`)
- Первый запуск может быть долгим
 
**Alt Linux 11**
```shell
apt-get install docker-engine docker-compose
```
**macOS**
```shell
brew install --cask docker
```
 
> ⚠️ В **Linux** не забудьте добавить пользователя в группу `docker`, чтобы работать без `sudo`:
> ```shell
> sudo usermod -aG docker $USER
> newgrp docker
> ```
> В **macOS** и **Windows** этого делать не нужно — Docker Desktop работает через виртуальную машину.
 
---
 
### Основные команды
 
#### Состояние и информация
 
Версия Docker:
```shell
docker version
```
или кратко:
```shell
docker --version
```
Мониторинг ресурсов в реальном времени:
```shell
docker stats
```
выйти из `stats` по **Ctrl+C**
 
Показать все контейнеры, включая остановленные:
```shell
docker ps -a
```
Показать все имеющиеся Docker-образы:
```shell
docker images
```
Быстрая демонстрация работы Docker:
```shell
docker run hello-world
```
Сводка по диску Docker:
```shell
docker system df
```
Сводка по всем томам:
```shell
docker volume ls
```
Список томов с размером:
```shell
docker system df -v
```
Артефакты и свободное место в buildx:
```shell
docker buildx du
```
Очистить все ненужные тома:
```shell
docker volume prune -a
```
Удаление всех остановленных контейнеров
```shell
docker container prune
```
```shell
docker image prune -a
```
Очистить кэш всех сборок:
```shell
docker builder prune -a
```
 
---
 
#### Образы
 
Получить список всех образов:
```shell
docker images
```
Показать детальную информацию по выбранному образу:
```shell
docker image inspect hello-world
```
Найти указанный образ в Docker Hub:
```shell
docker search nginx
```
Получить информацию по указанному образу:
```shell
docker inspect nginx
```
Скачать указанный образ:
```shell
docker pull nginx
```
Собрать образ из Dockerfile в текущей директории (`.`) и дать ему тег `my-app`:
```shell
docker build -t my-app .
```
Сканирование контейнера на наличие известных уязвимостей:
```shell
docker scout cves <image_name>
```
> ⚠️ `docker scan` — устаревшая команда. Используйте `docker scout` или `trivy`.
 
Показать лог контейнера:
```shell
docker logs <container_id>
```
Удалить указанный образ по имени:
```shell
docker image rm имя_образа
```
или короче:
```shell
docker rmi имя_образа
```
Удалить образ по его ID:
```shell
docker rmi id_образа
```
> ⚠️ `docker rm` удаляет **контейнеры**, а не образы. Для образов — `docker rmi`.
 
Удалить только промежуточные (dangling) образы без тегов:
```shell
docker image prune
```
Удалить все неиспользуемые образы с подтверждением:
```shell
docker image prune -a
```
Удалить все образы (принудительно):
```shell
docker rmi -f $(docker images -q)
```
 
---
 
#### Контейнеры
 
Получить список запущенных контейнеров:
```shell
docker ps
```
Получить список всех контейнеров, независимо от их состояния:
```shell
docker ps -a
```
Получить список контейнеров, из которых выполнен выход:
```shell
docker ps -a -f status=exited
```
Запустить контейнер в фоновом режиме (`-d`), пробросив порт 80 контейнера на порт 8080 хоста, с именем `my-container`:
```shell
docker run -d -p 8080:80 --name my-container <image_name>
```
Остановить контейнер:
```shell
docker stop my-nginx
```
Остановить все запущенные контейнеры:
```shell
docker stop $(docker ps -q)
```
Запустить остановленный контейнер:
```shell
docker start my-nginx
```
Зайти в контейнер в интерактивном режиме:
```shell
docker exec -it my-apache bash
```
Выполнить одну команду в контейнере без входа в shell:
```shell
docker exec my-apache ls -la
```
Удалить все остановленные или не запущенные (Exited, Created) контейнеры:
```shell
docker container prune
```
> **Prune** — удаляйте ненужные контейнеры, чтобы не засорять ваш Docker!
 
Удалить все контейнеры (включая запущенные — принудительно):
```shell
docker rm -f $(docker ps -aq)
```
Удалить только остановленные контейнеры:
```shell
docker rm $(docker ps -a -f status=exited -q)
```
Скопировать файл из контейнера на хост (и наоборот):
```shell
docker cp my-container:/path/to/file ./local-file
docker cp ./local-file my-container:/path/to/file
```
 
---
 
#### Сети
 
Показать все сети Docker:
```shell
docker network ls
```
Создать сеть:
```shell
docker network create my-net
```
Показать детали сети:
```shell
docker network inspect my-net
```
Подключить контейнер к сети:
```shell
docker network connect my-net my-container
```
Отключить контейнер от сети:
```shell
docker network disconnect my-net my-container
```
Проверить состояние сетевых подключений Docker-контейнеров:
```shell
docker network ls
```
 
---
 
#### Порты
 
Проверка указанного порта.
 
**Linux:**
```shell
netstat -tuln | grep :8082
```
**Windows:**
```powershell
netstat -aon | findstr :8082
```
Получить список проброшенных портов контейнера:
```shell
docker port <container_name>
```
> ⚠️ Без имени контейнера команда не работает.
 
Открыть в браузере страницу **Nginx** по динамически выбранному порту, например:
`http://localhost:32768/`
 
---
 
#### Тома
 
Показать все тома:
```shell
docker volume ls
```
Создать том:
```shell
docker volume create my-vol
```
Показать детали тома:
```shell
docker volume inspect my-vol
```
Удалить том:
```shell
docker volume rm my-vol
```
Удалить все неиспользуемые тома:
```shell
docker volume prune
```
 
---
 
#### Docker Compose
 
Запустить проект в фоне:
```shell
docker compose up -d
```
Остановить и удалить контейнеры и сети проекта (тома **сохраняются**):
```shell
docker compose down
```
Остановить и удалить контейнеры, сети **и тома** проекта:
```shell
docker compose down -v
```
Посмотреть статус сервисов проекта:
```shell
docker compose ps
```
Смотреть логи сервисов в реальном времени:
```shell
docker compose logs -f
```
Пересобрать образы проекта:
```shell
docker compose build
```
Перезапустить сервисы:
```shell
docker compose restart
```
Выполнить команду внутри сервиса:
```shell
docker compose exec <service> <command>
```
 
---
 
### DOCKER HUB
 
Найти указанный образ:
```shell
docker search nginx
```
Скачать указанный образ:
```shell
docker pull nginx
```
На самом деле это:
```shell
docker pull docker.io/library/nginx:latest
```
Получить информацию по указанному образу:
```shell
docker inspect nginx
```
Скачать образ **Postgres**:
```shell
docker pull postgres
```
Скачать образ **Redis**:
```shell
docker pull redis
```
Скачать образ **nginx на базе Alpine**:
```shell
docker pull nginx:alpine
```
Скачать образ **чистого Alpine Linux**:
```shell
docker pull alpine
```
Войти в Docker Hub:
```shell
docker login
```
Поставить тег образу для публикации:
```shell
docker tag my-app username/my-app:1.0
```
Опубликовать образ в Docker Hub:
```shell
docker push username/my-app:1.0
```
Выйти из Docker Hub:
```shell
docker logout
```
 
---
 
### Очистка (Prune)
 
| Команда | Что удаляет |
|---------|-------------|
| `docker container prune` | Остановленные контейнеры |
| `docker image prune` | Промежуточные (dangling) образы без тегов |
| `docker image prune -a` | Все неиспользуемые образы |
| `docker volume prune` | Неиспользуемые тома |
| `docker volume prune -a` | Все неиспользуемые тома (включая именованные) |
| `docker network prune` | Неиспользуемые сети |
| `docker builder prune` | Кэш сборок |
| `docker system prune` | Контейнеры + образы + сети + кэш (но **не тома**) |
| `docker system prune --volumes` | То же + **тома** |
| `docker system prune -a --volumes` | Всё неиспользуемое, включая образы с тегами и тома |
 
---
 
### Ресурсы
 
- [Что такое Docker?](/content/Docker/Docs/ThatIsDocker.md)
- [Codespace](/content/Docker/Docs/Codespace.md)
- [Dockerfile](/content/Docker/Docs/DockerfileInfo.md)
- [Dockerfile + Docker Compose](/content/Docker/Docs/Dockerfile&DockerCompose.md)
- [Жизненный цикл Docker-образа](/content/Docker/Docs/DockerImageLifecycle.md)
- [Docker Hub](/content/Docker/Docs/DockerHub.md)
- [docker stats](/content/Docker/Docs/dockerStats.md)
- [Docker-сети](/content/Docker/Docs/Network.md)
- [Portainer](/content/Docker/Docs/Portainer_info.md)
- [Docker + Продакшн (Production)](/content/Docker/Docs/Productiom.md)
- [docker container prune](/content/Docker/Docs/Prune.md)
- [Основное отличие Stop от Down](/content/Docker/Docs/stopDown.md)
 
> Если вы обнаружили ошибку в этом тексте — сообщите, пожалуйста, автору!
 
## Welcome to Docker
 
> Никогда в разработке не используйте русские имена файлов и каталогов!
 
> Никогда в разработке не используйте пробелы и спецсимволы в именах файлов и каталогов!
 
> Создание проекта лучше начать с "чистого листа", предварительно остановив и удалив все другие контейнеры и образы!
 
Это репозиторий для новых пользователей, начинающих работу с **Docker**
 
Для выполнения задания создайте в репозитории отдельную папку `Docker`, в ней папку `img` и папку `WelcomeToDocker` и в ней файл `README.md`.
 
Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)
 
> Перед созданием проекта убедитесь, что порт `8088` не занят другим приложением!
 
Проверить порт `8088` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8088
```
> Если эта команда ничего не возвращает, то порт свободен
 
Проверить порт `8088` для **Windows**:
```shell
netstat -aon | findstr :8088
```
 
Загрузить образ и запустить контейнера
```shell
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```
 
[Открыть http://localhost:8088 в браузере](http://localhost:8088)
 
 
Зайти в контейнер
```shell
docker exec -it welcome-to-docker /bin/sh
```
или
```shell
MSYS_NO_PATHCONV=1 docker exec -it welcome-to-docker /bin/sh
```
 
Повыполнять разные команды:
 
Показать ин-фу по ОС
```shell
uname -a
```
```shell
cat /etc/os-release
```
Диспетчер ресурсов
```shell
top
```
```shell
tree
```
Обновить источники приложений
```shell
apk update && apk upgrade
```
Установить приложение
```shell
apk add fastfetch
```
Запустить приложение
```shell
fastfetch
```
Выйти из контейнера
```shell
exit
```
 
Результаты работы с проектом прислать в виде ссылки на `README.md` с оформленным в **Markdowd** текстом с скриншотами по примеру с **Nginx**
 
> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору!
 
 ## Welcome to Docker
 
> Никогда в разработке не используйте русские имена файлов и каталогов!
 
> Никогда в разработке не используйте пробелы и спецсимволы в именах файлов и каталогов!
 
> Создание проекта лучше начать с "чистого листа", предварительно остановив и удалив все другие контейнеры и образы!
 
Это репозиторий для новых пользователей, начинающих работу с **Docker**
 
Для выполнения задания создайте в репозитории отдельную папку `Docker`, в ней папку `img` и папку `WelcomeToDocker` и в ней файл `README.md`.
 
Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)
 
> Перед созданием проекта убедитесь, что порт `8088` не занят другим приложением!
 
Проверить порт `8088` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8088
```
> Если эта команда ничего не возвращает, то порт свободен
 
Проверить порт `8088` для **Windows**:
```shell
netstat -aon | findstr :8088
```
 
Загрузить образ и запустить контейнера
```shell
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```
 
[Открыть http://localhost:8088 в браузере](http://localhost:8088)
 
 
Зайти в контейнер
```shell
docker exec -it welcome-to-docker /bin/sh
```
или
```shell
MSYS_NO_PATHCONV=1 docker exec -it welcome-to-docker /bin/sh
```
 
Повыполнять разные команды:
 
Показать ин-фу по ОС
```shell
uname -a
```
```shell
cat /etc/os-release
```
Диспетчер ресурсов
```shell
top
```
```shell
tree
```
Обновить источники приложений
```shell
apk update && apk upgrade
```
Установить приложение
```shell
apk add fastfetch
```
Запустить приложение
```shell
fastfetch
```
Выйти из контейнера
```shell
exit
```
 
Результаты работы с проектом прислать в виде ссылки на `README.md` с оформленным в **Markdowd** текстом с скриншотами по примеру с **Nginx**
 
> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору!