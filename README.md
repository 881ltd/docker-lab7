# Лабораторная работа №7 - Docker

## GitHub Codespaces (с iPhone)
Откройте **Code → Codespaces → Create codespace on main**, затем терминал.

### 1. Проверка Docker
```bash
docker --version
docker info
```

### 2. Docker Hub и Python
```bash
docker pull python
docker run -it python bash
```
В контейнере выполните `python --version`, затем `exit`.

### 3. Собственный образ
```bash
docker build -t lab7-python .
docker run --rm lab7-python
docker images
docker ps -a
```
Ожидается сообщение «Контейнер Python успешно запущен!» и версия Python.

### 4. Дополнительное задание nginx
```bash
docker run -d -p 8080:80 --name my-nginx nginx
docker ps
```
Откройте вкладку **Ports** в Codespaces и перейдите по ссылке порта 8080. На iPhone адрес `localhost:8080` не ведёт к Codespace.

### 5. Очистка
```bash
docker stop my-nginx
docker rm my-nginx
```

Для отчёта сделайте реальные скриншоты результатов команд и страницы nginx. Доступность Docker зависит от конфигурации Codespaces.
