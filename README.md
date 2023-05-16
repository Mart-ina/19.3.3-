# 19.3.3-
GET. POST. DELETE. PUT

Задание 19.3.3
Попробуйте использовать свободное API для написания запросов GET, POST, DELETE, PUT. Ваша задача — выполнить все запросы и напечатать при помощи команды print ответы запросов.

Обратите внимание на интересный ход: мы не можем быть уверены, что сервер вернёт ответ в формате json, поэтому сначала пытаемся декодировать полученные данные как json-строку. Если с этим возникают проблемы, то возвращаем ответ обычным текстом. 

 if 'application/json' in response.headers['Content-Type']:
                response.json()
            else:
                response.text
