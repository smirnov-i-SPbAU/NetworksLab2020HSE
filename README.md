# Описание протокола обмена

После соединениея клиент отправляет серверу сообщение в формате

* 4 байта -- длина имени в байтах (L)
* L байт -- имя как последовательность char
* 2 байта -- текущее время у клиента

При отправке нового сообщения в чат клиент посылает серверу сообщение в формате

* 4 байта -- длина сообщения в байтах (L)
* L байт -- сообщение как последовательность char

При поступлении нового сообщения на сервер, он отправляет всем клиентам сообщение в формате

* 2 байта -- время отправки сообщения 
* 4 байта -- длина сообщения в байтах (M)
* M байт -- сообщение как последовательность char
* 4 байта -- длина имени отправителя в байтах (S)
* S байт -- имя отправителя как последовательность char
