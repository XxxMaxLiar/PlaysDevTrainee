## Информационные коды
**100** — Continue — Временный код ответа, означающий начало принятия запроса к его последующей обработке. 

**101** — Switching Protocols — Сообщает о переключении сервера на протокол, которые был указан в заголовке Upgrade запроса клиента.

**102** — Processing — Информация о том, что запрос принят сервером и находится в обработке, но этот процесс еще не завершен.

**103** — Early Hints — Используется для предварительной загрузки данных пока сервер формирует полный ответ.

## Успешная обработка запроса
**200** — OK — Один из самых популярных ответов. Он свидетельствует о том, что обмен данными между клиентом и сервером прошли успешно. Именно код ответа 200 ждут от ресурса, чтобы проверить, что все работает как надо: сайт загружен, файл открывается и т.д.

**201** — Created — Информирует об успешном создании нового ресурса в результате выполнения запроса. Например, была создана новая страница. Если сервер по каким-то причинам не смог обработать запрос и ресурс не был создан, то код ответа будет 202.

**202** — Accepted — Сообщает, что сервер принял запрос, но не завершил его обработку.

**203** — Non-Authoritative Information — Отвечает об успешной обработке запроса с оговоркой на то, что передаваемая информация была предоставлена не из исходного сервера, а другого источника (например, резервной копии) и может быть неактуальной. 

**204** — No Content — Сообщает об успешном принятии и обработке запроса, а также о том, что у сервера нет содержимого для отправки пользователю.

**205** — Reset Content — Сервер передает пользователю ответ в виде требований к сбросу введенных данных. Например, о необходимости очистить форму с заполненными до этого данными.

**206** — Partial Content — Свидетельствует о частичном выполнении GET-запроса сервером, возвращая только запрошенную пользователем часть контента. Этот код встречается при использовании кэширования.

## Коды редиректов
**300** — Multiple Choices — Ответ срабатывает при условии, что по указанному запросу существует несколько вариантов URL. При таком варианте пользователь или User-agent должен выбрать альтернативный адрес.

**301** — Moved Permanently — Свидетельствует о перемещении ранее проиндексированного URL на новый адрес.

**302** — Found, 302 Moved Temporarily — Сообщает, что ранее проиндексированный URL был временно перемещен по другому адресу. При этом страница остается в индексе, а в ответе указывается новый адрес запрашиваемого URL.

**303** — See Other — Указывает пользователю, что запрошенная страница находится по другому адресу с запросом GET. 

**304** — Not Modified — Показывает, что запрашиваемая страница или объект не были изменены с момента последнего обновления кэша данного документа.

**305** — Use Proxy — Сообщает пользователю, что запрашиваемый ресурс доступен только через прокси. Данные по прокси указаны в ответе сервера.

**307** — Temporary Redirect — Код схож с 302, сообщая о временном перемещении ресурса на другой адрес. Разница заключается в способе обращения к ресурсу, который должен быть получен тем же методом, что и предыдущий запрос.

## Ошибки клиента

Коды состояний данной группы сообщают об ошибках клиента, при которых сервер не может вызвать запрашиваемый результат.

**400** — Bad Request — Ошибка свидетельствует от том, что сервер не понял запрос пользователя из-за синтаксической ошибки.

**401** — Unauthorized — Сообщает о необходимости быть авторизованным для получения запрашиваемого доступа. Возникает при неправильном вводе данных пользователем при авторизации. 

**403** — Forbidden — Запрет доступа к запрашиваемой странице. Доступ может быть ограничен настройками индексации или запрещен для определенных IP.

**404** — Пожалуй, самая распространенная ошибка. Сообщает о том, что запрашиваемая страница не найдена. Самая частая причина — ошибка в написании адреса.

**405** — Method Not Allowed — Сообщает, что в запросе используется метод, который не поддерживается сервером.

**406** — Not Acceptable — Указывает, что запрашиваемый пользователем контент не может быть распознан. Причины могут быть в кодировке, методе сжатия или формате объекта. 

**407** — Proxy Authentication Required — Сообщает, что доступ может быть предоставлен только при авторизации через прокси-сервер. 

**408** — Request Timeout — Сервер прервал соединение с пользователем из-за слишком долгого ожидания. Данный ответ не возвращается если пользователь принудительно отменил запрос или соединение прервалось по иным причинам.

**409** — Conflict — Посылаемый пользователем запрос вызывает конфликт с сервером или другим обращением. 

**410** — Gone — Ответ сервера при запросе к странице или объекту, который был удален и более недоступен.

**411** — Length Required — Отказ сервера на обработку запроса если в нем не указан Content-Length заголовка.

**413** — Request Entity Too Large — Сервер не может обработать обращение из-за слишком большого размера запроса.

**414** — Request-URL Too Long — Сервер не может обработать обращение если в запросе указан слишком длинный URL.

**415** — Unsupported Media Type — Формат запроса пользователя не может быть обработан. Такое встречается при загрузке данных неподходящего формата. 

**416** — Requested Range Not Satisfiable — Отказ сервера на выполнение запроса из-за некорректного значения поля Range. 

**417** — Expectation Failed — Отказ сервера на выполнение запроса из-за некорректного значения поля Expect. 

**422**— Unprocessable Entity — Сервер принял и распознал запрос, но не может его выполнить из-за наличия логической ошибки.

**423** — Locked — Запрашиваемая пользователем страница заблокирована. Как правило, это делается для защиты содержимого данной страницы или объекта.

**424** — Failed Dependency — Выполнение текущего запроса зависит от исхода других связанных с ней операций. Если условия не будут соблюдены, то соединение будет разорвано. 

**426** — Upgrade Required — Ошибка указывает на необходимость обновить протокол. Встречается, когда сервер запрашивает https-соединение, которое не может быть предоставлено клиентом.

**429** — Too Many Requests — Возникает при превышении лимита отправляемых пользователем запросов за короткий промежуток времени. Часто используется настройками безопасности.

## Ошибки сервера

В эту группу входят коды ошибок со стороны сервера, когда по тем или иным причинам он не способен обработать запрос или выполнить требуемую операцию. 

**500** — Internal Server Error — Код оповещает о возникшей внутренней ошибке сервера или его аварийном отказе. 

**501** — Not Implemented — Сервер столкнулся с запросом, который не смог распознать. Либо запрос не поддерживается и не может быть обработан. 

**502** — Bad Gateway — Сообщает о неправильном получении ответа вышестоящего сервера. Частая причина — несогласованные протоколов между шлюзом и сервером (ошибки DNS, прокси, хостинга).

**503** — Service Unavailable — Указывает на временную недоступность сервера. Причиной может быть его перезагрузка, техническое обслуживание, обращение слишком большого количества пользователей при наличии подобных ограничений. Как правило, сообщение об ошибке содержит параметр Retry-After, информирующий о времени восстановления штатной работы ресурса.

**504** — Gateway Time-out — Истек срок ожидания ответа от вышестоящего сервера. Возможные причины: недостаток ресурсов, неполадки с сетевым соединением, ошибки HTTP протокола, настроен слишком короткий срок ожидания.

**505** — HTTP Version Not Supported — Используемая в запросе версия протокола HTTP не поддерживается сервером. Встречается при использовании устаревшего формата HTTP-протокола.

**506** — Variant Also Negotiates — Сервер не может обработать запрос из-за его неправильной настройки. Сервер зацикливает ответ на себя, выдавая ошибку.

**507** — Insufficient Storage — Означает нехватку места на сервере для обработки запросов пользователя. Нужно освободить или увеличить память, либо обратиться в техническую поддержку.

**508** — Loop Detected — Ошибка возникает в связи с бесконечным перенаправлением. При обработке запроса возникает петля, что приводит к завершению операции.

**509** — Bandwidth Limit Exceeded — Превышен установленный лимит потребления трафика. Ошибка актуальная для интернет-каналов с ограничением по трафику.

**510** — Not Extended — Сервер не поддерживает и не может отработать запрашиваемое пользователем расширение. В теле ошибки может быть приведен список доступных расширений.

**511** — Network Authentication Required — Сообщает о необходимости авторизации для доступа к сети. Например, если пользователь не авторизовался при подключении к Wi-Fi.