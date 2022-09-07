# Пульт охраны банковского хранилища

Программа ведет учет посещений банковского хранилища. Без доступа к БД, запустить скрипт не получиться.

### Как установить

Python3 должен быть уже установлен. 
Затем используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```
Необходимо создать файл с секретными данными - `.env`
```
DB_HOST=<host>
DB_PORT=<port>
DB_NAME=<name>
DB_USER=<user>
DB_PASSWORD=<password>
DATABASE_URL=postgres://${DB_USER}:${DB_PASSWORD}@${DB_HOST}:${DB_PORT}/${DB_NAME}
SECRET_KEY=<secret key>
DEBUG=True or DEBUG=False
ALLOWED_HOSTS=<allowed_host>,<allowed_host>,<allowed_host>
```
После установки зависимостей запустите сервер командой:
```
python manage.py runserver
```
Сервер запускается по ссылкам:
```
http://127.0.0.1:8000
```
```
http://localhost:8000/
```