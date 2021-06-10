# mis-deploy

## Требования

- Linux или Windows 10 с WSL 2
- Docker, docker-compose
- python3.9

## Скрип запуска

```sh
git submodule init
git submodule update
docker-compose up —build -d

cd mis-backend
python3.9 -m venv venv
. ./venv/bin/activate
pip install -r requirements.txt
alembic upgrade head
python db_init.py
```

Сайт будет доступен по http://localhost:8080
