# technopark_proxy
## Запуск в докере
`sudo docker build -t proxy .`\
`sudo docker run -d -p 8080:8080 -p 8000:8000 -t proxy`

## Запуск локально

`go run cmd/main.go`

## Проверка работы прокси-сервера

`curl -i -x 127.0.0.1:8080 https://www.wikipedia.org/`\
`curl -i -x 127.0.0.1:8080 http://mail.ru`\
`curl -i 127.0.0.1:8000/requests`\
`curl -i  127.0.0.1:8000/requests/1`\
`curl -i  127.0.0.1:8000/repeat/1`
