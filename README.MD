# Тестовое задание Lev Usachev DevOps

Простое веб-приложение на Python за Nginx reverse proxy, запуск через Docker Compose.


## Запуск

```bash
git clone https://github.com/fuandtmp/em-usachev-task-test.git
cd em-usachev-task-test
docker compose up -d --build
```

## Проверка

```bash
curl http://localhost
```

Ожидаемый ответ:
```
Hello from Effective Mobile!
```

## Остановка

```bash
docker compose down
```

## Как устроено
 
```
Клиент → :80 → Nginx (reverse proxy) → :8080 → Python backend
```

## Структура проекта

```
├── backend/
│   ├── Dockerfile
│   └── app.py
├── nginx/
│   └── nginx.conf
├── docker-compose.yml
├── .gitignore
└── README.md
```

## Стек

- Python 3.12 (alpine, http.server)
- Nginx 1.27 (alpine)
- Docker Compose