# JS_Week19
Hometask, JS Week 19, HTTP, API, Get/Post methods, Promises

# Вопросы 💎

1. Опишите разницу между синхронными и асинхронными функциями.

*Синхронные функции выполняются построчно и последовательно, сверху вниз. 
Асинхронные делают остановку, выполняют код далее и после могут возвращаться к тому, чтобы было прописано ранее по вызову функции.*

2. Сравните подходы работы с асинхронным кодом: *сallbacks* vs *promises* vs *async / await

Колбэк функция вызывается в ответ на совершенное действие. Ее минус - это возможность возникновения ада колбэков, когда есть ряд задач, зависящих друг от друга и возникает длинная цепочка из функций. 
Промисы описывают код, который выполнится только после того, как произойдет какое-то событие. Принимает на вход 2 колбэка - резолвд и реджектид - в зависимости от того, выполнен код или нет. Также у промисов есть методы, которые описывают что сделать в случае исполнения кода, либо ошибки (then, catch, finally).
Связка async/await позволяет сократить код, который может быть описан в промисах, заменяя then или колбэки с помощью await.*

3. Что такое цикл событий (event loop) в JS ?

*Event loop это цикл обработки событий в JS.*

4. Какая разница между «стеком вызовов» (call stack) и «очередью задач» (task queue)?

*Стек и очередь - это структуры данных, используемые для хранения элементов данных. 
Основное различие в том, что стек следует принципу last-in, first-out (LIFO), очередь -  first-in, first-out (FIFO).*

5. Какие версии HTTP-протокола вам известны?

*Стандарт HTTP/0.9 – версия протокола HTTP 0.9, RFC 1945 (стандарт HTTP/1.0), стандарт HTTP/1.1, HTTP 2*

6. Какие знаете коды ответа (состояния) HTTP?

*200 OK («хорошо»), 404 Not Found, 400 Bad Request, 500 Internal Server Error*

7. Как клиент взаимодействует с сервером?

*Клиент может взаимодействовать с сервером с помощью HTTP запросов: 
get, post, delete, put и patch. С помощью запроса get можно получать данные с сервера, а с помощью запроса post можно добавлять данные на сервер.* 

8. Самостоятельно разберитесь, что такое Cross-Origin Resource Sharing? Как устранить проблемы с CORS?

*CORS - это механизм, который позволяет получать доступ к ресурсам сервера, расположенного на отличном от текущего домена.* 
*Решить возникающие проблемы с CORS можно при помощи Proxy сервера, а также можно запустить специальный инстанс браузера, в котором отключены CORS.*

9. Самостоятельно разберитесь, что такое REST?

*REST (Representational state transfer) – это стиль архитектуры программного обеспечения для распределенных систем, таких как World Wide Web, который, как правило, используется для построения веб-служб. EST является очень простым интерфейсом управления информацией без использования каких-то дополнительных внутренних прослоек. Каждая единица информации однозначно определяется глобальным идентификатором, таким как URL. Каждая URL в свою очередь имеет строго заданный формат.*

10. Как посмотреть заголовки запроса к странице или API?

*Inspect → Network → выбираем Name → Headers*

11. Что можно писать в параметре заголовков `Content-Type` ?

*В ответах сервера заголовок `Content-Type` сообщает клиенту, какой будет тип передаваемого контента. Можно указывать `application/x-www-form-urlencoded`, `multipart/form-data`,  `text/plain`, `application/json` (чтобы послать в теле запроса данные в JSON, нужно передать в заголовках тип `application/json`).*

12. Давайте отправим информацию о собачке в API по адресу `localhost/pets/add` 

*fetch('localhost/pets/add', {
method: 'POST',
body: JSON.stringify({
"breed": "Beagle",
"size": "large",
"color": "orange",
"age": 6
})
});*
