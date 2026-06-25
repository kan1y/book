---
title: "Микросервисы и API"
author: "Хосе Аро Перальта"
topics: [микросервисы, API, интеграция, аутентификация, OAuth]
chapters: [11, 12]
---

**==> picture [398 x 223] intentionally omitted <==**

**==> picture [395 x 177] intentionally omitted <==**

## 

**==> picture [31 x 15] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [81 x 19] intentionally omitted <==**

**==> picture [360 x 32] intentionally omitted <==**

**==> picture [80 x 7] intentionally omitted <==**

**https://t.me/it_boooks/2** 

## 

## 

|Предисловие..|..16|
|---|---|
|Благодарности.|. .18|
|Окниге......|.20|
|Комустоитпрочитатьэтукнигу.|.20|
|Структураиздания. . . .|.20|
|Окоде............|.23|
|Другиеонлайн-ресурсы.|.24|
|Обавторе...........|.25|
|Иллюстрациянаобложке.|.26|
|Онаучныхредакторахрусскоязычногоиздания.|.27|
|Отиздательства. . . . . . . . . . . . . . . . . . . . .|.28|



## 

|Часть**1.**Представляем**API**микросервисов||
|---|---|
|Глава**1.**ЧтотакоеАРIмикросервисов.. .|.31|
|1.1.Чтотакоемикросервисы.. . . . . .|.32|
|1.1.1.Определениемикросервисов|.32|
|1.1.2.Микросервисыпротивмонолитов.|. 33|
|1.1.3.Историяпоявлениясовременныхмикросервисов.|. 36|
|1.2.Чтотакоевеб-АРI|.37|
|1.2.1. API. . . .|.37|
|1.2.2.Веб-АРI.. .|. 38|
|1.2.3.КакAPIпомогаютнамуправлятьинтеграциеймикросервисов|. 38|



|1.3.Проблемымикросервиснойархитектуры. . .|. 40|
|---|---|
|1.3.1.Оптимальнаядекомпозициясервиса. .|.41|
|1.3.2.Интеграционныетестымикросервисов.|.41|
|1.3.3.Обработканедоступностисервиса.. . .|. 42|
|1.3.4.Трассировкараспределенныхтранзакций.|. 43|
|1.3.5.Повышениесложностиэксплуатацииинакладныхрасходов||
|наинфраструктуру. . . . . . . . . . . . . . . . . . . . . . . .|. 44|
|1.4.Введениевразработкучерездокументирование(DDD).|. 45|
|1.5.ЗнакомствосприложениемCoffeeMesh|. 47|
|1.6.Длякогоэтакнигаи чемувынаучитесь|. 47|
|Резюме.. . . . . . . . . . . . . . .|.48|
|ва**2.**РазработкапростогоAPI .|. 50|
|2.1.ЗнакомимсясоспецификациейAPIсервисазаказов.|.51|
|2.2.Высокоуровневаяархитектураприложениязаказов. . .|. 52|
|2.3.Реализация эндпоинтовAPI. . . . . . . . . . . . . . . . . . .|. 53|
|2.4.Реализациямоделейвалидацииданныхспомощьюpydantic .|. 60|
|2.5.Валидацияполезнойнагрузкизапросаспомощьюpydantic.|. 65|
|2.6.Маршалингивалидацияполезнойнагрузкиответа||
|спомощьюpydantic. . . . . . . . . . . . . . . . . . . . . . . . . . .|. 69|
|2.7.ДобавлениевAPIсохраненноговпамятисписказаказов|. 73|
|Резюме.. . . . . . . . . . . . . . . . . . . .|. 75|
|ва**3.**Проектированиемикросервисов.|. 76|
|3.1.ПредставляемCoffeeMesh . . . . . . .|. 77|
|3.2.Принципыпроектированиямикросервисов.|. 77|
|3.2.1.Принцип«Базаданныхдлякаждогосервиса»|. 77|
|3.2.2.Принципслабойсвязашюсти.. . . . . . .|. 79|
|3.2.3.Принципединственнойответственности|. 80|
|3.3.Декомпозициясервисовпобизнес-функциям.|. 80|
|3.3.1.Анализбизнес-структурыCoffeeMesh . .|.81|
|3.3.2.Декомпозициямикросервисовпофункциям. .|.81|
|3.4.Декомпозициясервисовпоподдоменам. . . . . . . . .|. 84|
|3.4.1.Чтотакоепредметно-ориентированноепроектирование.|. 84|
|3.4.2.ПрименениестратегическогоанализавCoffeeMesh. . . .|. 85|
|3.5.Декомпозицияпобизнес-функциямвсравнениисдекомпозицией||
|поподдоменам.|. 89|
|Резюме...................................... . . . .|.90|



## 

## 

## 

|Часть**11.**Проектированиеиразработка**RESTAPI**||
|---|---|
|Глава4.ПринципыпроектированияREST API . . . . . .|. 93|
|4.1.ЧтотакоеREST. . . . . . . . . . . . . . . . . . . . . .|.94|
|4.2.АрхитектурныеограниченияприложенийREST.|.95|
|4.2.1.Разделениезадач:принципклиент-сервернойархитектуры.|. 96|
|4.2.2.Добавляеммасштабирование:принципотсутствия||
|записисостояния. . . . . . . . . . . . . . . . . . . . . . . . . .|.97|
|4.2.3.Оптимизацияпроизводительности:принципкэшируемости.|.97|
|4.2.4.Упрощениедляклиента:принципмногоуровневойсистемы.|. 98|
|4.2.5.Расширяемыеинтерфейсы:принцип<<кодпозапросу,>.. . . .|. 99|
|4.2.6.Сохранениесогласованности:принципединстваинтерфейса|. 100|
|4.3.Гипермедиакак двигательсостоянияприложений. .|. 100|
|4.4.АнализзрелостиAPIспомощьюмоделиРичардсона.|. 103|
|4.4.1.УровеньО.Веб-АРIвстилеRPC.. . . . . . . . .|. 104|
|4.4.2.Уровень1.Введениепонятияресурса.. . . . . .|. 105|
|4.4.3.Уровень2.ИспользованиеметодовНТТРистатус-кодов.|. 106|
|4.4.4.Уровень3.ВозможностьобнаруженияAPI . . . . . . . .|106|
|4.5.СтруктурированныеURL-aдpecaресурсовсметодамиНТТР|107|
|4.6.Использованиестатус-кодовНТТРдлясоздания||
|информативныхНТТР-ответов. . . . . . . . . . . . . . . . . . . .|111|
|4.6.1.Чтотакоестатус-кодыНТТР.. . . . . . . . . . . . . .|111|
|4.6.2.Использованиестатус-кодовНТТРдлясообщения||
|обошибкахклиентавзапросе. . . . . . . . . . . . . . . . . .|112|
|4.6.3.Использованиестатус-кодовНТТРдлясообщения||
|обошибкахпа сервере. . . . . . . . . . . . . . . . . . . . . . .|116|
|4.7.ПроектированиеполезнойнагрузкиAPI.. . . . . . . . . . .|117|
|4.7.1.ЧтотакоеполезнаянагрузкаНТТРикогдамыееиспользуем.|. 118|
|4.7.2.МоделипроектированияполезнойнагрузкиНТТР.|. 119|
|4.8.ПроектированиепараметровзапросаURL.|. 123|
|Резюме.. . . . . . . . . . . . . . . . . . . . . . . . .|. 124|
|Глава**5.**ДокументированиеREST APIспомощьюOpenAPI.|. 125|
|5.1.ИспользованиеJSОNSchemaдлямоделированияданных.|. 126|
|5.2.СтруктураспецификацииOpenAPI . . . . . . .|. 130|
|5.3.ДокумептированиеэндпоиптовAPI. . . . . . .|.132|
|5.4.ДокументированиепараметровзапросаURL .|. 133|
|5.5.Документированиеполезнойнагрузкизапросов.|. 134|
|5.6.Рефакторингопределенийсхемвоизбежаниеповторов.|. 136|



|5.7.ДокументированиеответовAPI........|.|.....139|
|---|---|---|
|5.8.Созданиеобщихответов. . . . . . . . . . . . .|.|.....142|
|5.9.ОпределениесхемыаутентификацииAPI..|.|.....144|
|Резюме.........................||..146|
|Глава**6.**РазработкаREST APIнаPython. . . . .||. . 147|
|6.1.ОбзорAPIсервисазаказов.. . . . . . . . .||..148|
|6.2.ПараметрыURL-зaпpocaдляAPIсервисазаказов.||. . 149|
|6.3.Валидацияполезнойнагрузкиснеизвестнымиполями............152|||
|6.4.ПереопределениединамическигенерируемойспецификацииFastAPI...156|||
|6.5.ОбзорAPIсервисакухни.. . . . . . . . . . . .||. . 157|
|6.6.Вводимвработуflask-smorest..........||. . 159|
|6.7.Инициализациявеб-приложениядляAPI..||....161|
|6.8.РеализацияэндпоинтовAPI. . . . . . . . . . . . .||. . 163|
|6.9.Реализациямоделейпроверкиполезнойнагрузки|||
|спомощьюmarshmallow . . . . . . . . . . . . . . . . . . . .||..167|
|6.10.ПроверкапараметровзапросаURL.........||. .171|
|6.11.Проверкаданныхпередсериализациейответа..||. . 174|
|6.12.Реализацияспискарасписанийвпамяти......||. . 178|
|6.13.ПереопределениединамическигенерируемойспецификацииAPI|||
|flask-smorest. . . . . . .||. . 180|
|Резюме.........................||..181|
|Глава**7.**Паттерныреализациисервисов.. . . . .||....183|
|7.1.Гексагоналы1ыеархитектурыдлямикросервисов.||. . 184|
|7.2.Настройкасредыиструктурыпроекта........|.|.....187|
|7.3.Реализациямоделейбазданных............|.|.....189|
|7.4.РеализацияпаттернаРепозиторийдлядоступакданным..||....195|
|7.4.1.ПаттернРепозиторий:чтоэтои чемонполезен.............195|||
|7.4.2.РеализацияпаттернаРепозиторий. . . . . . . .||. . 197|
|7.5.Реализацияуровнябизнес-логики.............||. . 202|
|7.6.ВнедрениепаттернаЕдиницаработы...........||. . 212|
|7.7.ИнтеграцияуровняAPIиуровнясервиса........|.|.....217|
|Резюме.....................................||....221|



## 

|Часть**111.**Проектированиеиреализация**Graph**|**QLAPI**|
|---|---|
|Глава**8.**ПроектированиеGraphQL API..........|. . 225|
|8.1.ЗнакомствосGraphQL............|. . 226|
|8.2.ПредставляемAPIсервисапродукции......|. . 229|



|8.3.ЗнакомствоссистемойтиповGraphQL. . . . . . . . . . . . . . . . . . . . .|. 232|
|---|---|
|8.3.1.Созданиеопределенийсвойствспомощьюскалярныхвеличин.|. 232|
|8.3.2.Моделированиересурсовсиспользованиемобъектныхтипов.|. 233|
|8.3.3.Созданиекастомныхскалярныхвеличин. . . . . . .|. 235|
|8.4.Представлепиеколлекцийэлементовспомощьюсписков.|. 236|
|8.5.Мыслитеграфически:выстраиваниезначимыхсвязей||
|междуобъектпымитипами. . . . . . . . . . . . . . . . . . .|. 237|
|8.5.1.Соединениетиповспомощьюсвойств-ребер. . .|. 237|
|8.5.2.Созданиесоединенийсосквозпыми типами. . .|. 239|
|8.6.Сочетаниеразличпыхтиповспомощьюобъединенийииптерфейсов|.241|
|8.7.Ограничениезначенийсвойствспомощьюперечислений.|. 244|
|8.8.ОпределениезапросовдляполученияданныхизAPI.|. 245|
|8.9.Изменениесостояниясервераспомощьюмутаций.|. 248|
|Резюме.. . . . . . . . . . . . . . . . . .|.251|
|Глава**9.**ИспользованиеGraphQL API .|. 253|
|9.1.Запускmock-cepвepaGraphQL.|. 254|
|9.2.ЗапросыGraphQL . . . . . . . . .|. 256|
|9 .2.1.Выполнениепростыхзапросов.|. 256|
|9.2.2.Выполнениезапросовспараметрами.|. 257|
|9.2.3.Ошибкизапросов. . . . . . . . . . . . .|. 258|
|9.3.Использованиефрагментоввзапросах. . . .|. 260|
|9.4.Выполнениезапросовсвходнымипараметрами.|. 262|
|9.5.НавигацияпографуAPI . . . . . . . . . . . . . . . .|. 262|
|9.6.Выполнениенесколькихзапросовиалиасинг.. .|. 264|
|9.6.1.Выполнениенесколькихзапросовзаодинраз|. 264|
|9.6.2.Алиасингзапросов.. . . . . . . . . . . . . . . . .|. 265|
|9.7.ВыполнениемутацийGraphQL. . . . . . . . . . . . . .|. 268|
|9.8.Выполнениепараметризованныхзапросовимутаций|. 269|
|9.9.РаскрываемтайнызапросовGraphQL . . . . . . .|. 273|
|9.10.ВызовGraphQL APIспомощьюкоданаPython|. 274|
|Резюме.. . . . . . . . . . . . . . . . . . . . . . . . . . .|. 276|
|Глава**10.**СозданиеGraphQL APIспомощьюPython|. 277|
|10.1.АнализтребованийкAPI.|. 278|
|10.2.Технологическийстек.. .|. 278|
|10.3.ФреймворкAriadne . . . .|. 280|
|10.4.РеализацияAPIсервисапродукции.|. 286|
|10.4.1.Разработкаструктурыпроекта|. 286|



## 

|10.4.2.СозданиеточкивходадлясервераGraphQL....||. . 287|
|---|---|---|
|10.4.3.Реализациярезольверовзапросов. .||..288|
|10.4.4.Реализациярезольверовтипов....||..291|
|10.4.5.Обработкапараметровзапроса....||. . 298|
|10.4.6.Реализациярезольверовмутаций........||. . 301|
|10.4.7.Созданиерезольверовдлякастомныхскалярных|типов...|. . 304|
|10.4.8.Реализациярезольверовполей. . . . . .|. . . . . . .|. . 308|
|Резюме......||..311|



## 

|иразвертывание**API**микросервисов||
|---|---|
|Глава**11.**Авторизация иаутентификацияAPI........|. . 315|
|11.1.Настройкасредыдляпримеровэтойглавы..|. . 316|
|11.2.Протоколыаутентификациииавторизации..|. . 317|
|11.2.1.ЧтотакоеOpen Authorization .|. . 317|
|11.2.2.ЧтотакоеOpenlDConnect...|. . 323|
|11.3.РаботаcJSONWebTokens..|. . 325|
|11.3.1.ЗаrоловокJWТ.....|. . 327|
|11.3.2.УтвержденияJWТ...|....328|
|11.3.3.СозданиеJWТ..|....330|
|11.3.4.ПроверкаJWТ......|. . 332|
|11.3.5.ВалидацияJWТ.....|. . 334|
|11.4.ДобавлениеавторизациинаAPIсервера........|. . 335|
|11.4.1.Созданиемодуляавторизации..........|. . 337|
|11.4.2.Созданиепромежуточногопрограммногообеспечения||
|дляавторизации. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .|. . 338|
|11.4.3.ДобавлениепромежуточногопрограммногообеспеченияСОRS . . 341||
|11.5.Авторизациядоступак ресурсам..........................343||
|11.5.1.Обновлениебазыданныхдляпривязкипользователейизаказов. . 343||
|11.5.2.Ограничениедоступапользователейкихсобственнымресурсам..346||
|Резюме.. . . . . . . . . . . . . . . . . . . . . .|. . 350|
|Глава**12.**ТестированиеивалидацияAPI...|..352|
|12.1.НастройкасредыдлятестированияAPI . . . .|..353|
|12.2.ТестированиеRESTAPIспомощьюDredd..|. . 354|
|12.2.1.ЧтотакоеDredd................|. . 355|
|12.2.2.УстановкаизапускнаборатестовDreddпоумолчанию.|....356|
|12.2.3.НастройканаборатестовDreddспомощьюхуков..|. . 358|
|12.2.4.ИспользованиеDreddдлятестированияAPI........|....366|



|12.3.Введениевтестированиенаосновесвойств. . . . .|. 366|
|---|---|
|12.3.1.Чтотакоетестированиепаоснове свойств..|. 366|
|12.3.2.ТрадиционныйподходктестированиюAPI.|. 367|
|12.3.3.ТестированиепаосновесвойствсиспользованиемHypothesis .|. 369|
|12.3.4.ИспользованиеHypothesisдлятестированияэпдпоипта||
|RESTAPI.. . . . . . . . . . . . . . . . . . . . . . . . . . . . . .|. 371|
|12.4.ТестированиеREST APIспомощьюSchemathesis . . . . .|. 374|
|12.4.1.ЗапускнаборатестовSchemathesisпоумолчанию.|. 375|
|12.4.2.Использованиессылокдлярасширениянабора||
|тестовSchemathesis . . . . . . . . . . . . . . . . . . . . . . . . .|. 375|
|12.5.ТестированиеGraphQL API . . . . . . . . . . . . . . . . . . .|. 379|
|12.5.1.ТестированиеGraphQL APIспомощьюSchemathesis.|. 380|
|12.6.РазработкастратегиитестированияAPI|. 382|
|Резюме.. . . . . . . . . . . . . . . . . . . . . . . .|. 382|
|Глава**13.**КонтейнеризацияAPIмикросервисов..|. 384|
|13.1.Настройкасредыдляэтойглавы. . . . . .|. 385|
|13.2.Контейнеризациямикросервиса. . . . . .|. 386|
|13.3.ЗапускприложенийспомощьюDocker Compose. .|. 391|
|13.4.ПубликацияDосkеr-образоввреестреконтейнеров.|. 393|
|Резюме.. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .|. 395|
|Глава**14.**РазвертываниеAPIмикросервисовспомощьюKubernetes|. 396|
|14.1.Настройкасредыдляэтойглавы. . . . . . . . . .|. 398|
|14.2.КакработаетKubernetes:версияCliffsNotes . . . . . . . . . . . .|. 399|
|14.3.СозданиекластераKubernetesспомощьюEKS.. . . . . . . . .|.401|
|14.4.ИспользованиеролейIAMдляучетныхзаписейсервисовKubemetes|. 405|
|14.5.РазвертываниебалансировщиканагрузкиKubemetes.|. 406|
|14.6.РазвертываниемикросервисоввкластереKubernetes.|. 409|
|14.6.1.Созданиеобъектаразвертывания.. . . . . . . . .|. 410|
|14.6.2.Созданиеобъектасервиса. . . . . . . . . . . . . .|. 413|
|14.6.3.Предоставлениедоступаксервисамспомощьюingress-oбъeктoв|..415|
|14.7.НастройкабессервернойбазыданныхспомощьюАWSAurora. .|. 417|
|14.7.1.СозданиебессервернойбазыданныхAurora. . . . . . . .|. 417|
|14.7.2.УправлениесекретамивKubernetes. . . . . . . . . . . . .|. 420|
|14.7.3.Запускмиграциибазыданныхиподключениесервиса||
|кбазеданных.. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .|. 424|
|14.8.ОбновлениеспецификацииOpenAPIсуказаниемименихостаALB|. 427|
|14.9.УдалениекластераKubemetes.|. 430|
|Резюме.. . . . . . . . . . . . . . . . . .|. 432|



## 

|Приnожения||
|---|---|
|ПриложениеА.Типывеб-АРI ипротоколов.....|. . 434|
|А.1.РассветАР!:RPC, XML-RPCиJSON-RPC.|. . 435|
|А.2.SOAPипоявлениестандартовАР!......|. . 437|
|А.3.RPCсновананоситудар:быстрыйобменданнымичерезgRPC.|. . 439|
|А.4.АР!НТТРиREST . . . . . . . . . . . . . . . . . . . . . . . .|..441|
|А.5.ДетализированныезапросысиспользованиемGraphQL..|. . 443|
|ПриложениеБ.УправлениежизненнымцикломАР!.........|. . 446|
|Б.1.СтратегииуправленияверсиямидляразвивающихсяАР!. . . . . .|<br>..447|
|Б.2.ВыводАР!изэксплуатации..........................|. . 449|
|ПриложениеВ.АвторизацияАР!сиспользованием||
|поставщикаудостоверений..................|..451|
|В.1.Использованиепоставщикаудостоверенийкакуслуги.|. . 452|
|В.2.ИспользованиесхемыавторизацииРКСЕ. . . . . . . . .|. . 458|
|В.3.Использованиесхемыучетныхданныхклиента. . . . . .|. . . . 459|
|В.4.АвторизациязапросоввпользовательскоминтерфейсеSwagger . .|. . . . 461|



## 

## 

## 

## 

## 

## 

## 

**==> picture [99 x 139] intentionally omitted <==**

## 

# 

## 

## 

**==> picture [371 x 169] intentionally omitted <==**

**https://t.me/it_boooks/2** 

**==> picture [367 x 126] intentionally omitted <==**

## 

## 

## 

**==> picture [331 x 114] intentionally omitted <==**

## 

**==> picture [369 x 264] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [353 x 97] intentionally omitted <==**

## 

## 

**==> picture [315 x 158] intentionally omitted <==**

## 

**==> picture [355 x 211] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [269 x 252] intentionally omitted <==**

## 

**==> picture [371 x 174] intentionally omitted <==**

## 

## 

## 

**==> picture [358 x 337] intentionally omitted <==**

## 

## 

## 

**==> picture [369 x 176] intentionally omitted <==**

**https://t.me/it_boooks/2** 

**==> picture [367 x 146] intentionally omitted <==**

## 

## 

**==> picture [367 x 141] intentionally omitted <==**

## 

**==> picture [358 x 78] intentionally omitted <==**

**==> picture [340 x 103] intentionally omitted <==**

## 

## 

**==> picture [233 x 289] intentionally omitted <==**

## 

**==> picture [177 x 40] intentionally omitted <==**

**==> picture [160 x 30] intentionally omitted <==**

**==> picture [301 x 140] intentionally omitted <==**

**==> picture [371 x 242] intentionally omitted <==**

**==> picture [371 x 238] intentionally omitted <==**

## 

## 

## 

**==> picture [193 x 9] intentionally omitted <==**

## 

**==> picture [187 x 63] intentionally omitted <==**

## 

**==> picture [369 x 477] intentionally omitted <==**

## 

**==> picture [118 x 39] intentionally omitted <==**

**==> picture [310 x 288] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [350 x 357] intentionally omitted <==**

## 

**==> picture [369 x 242] intentionally omitted <==**

## 

## 

**==> picture [314 x 106] intentionally omitted <==**

## 

## 

**==> picture [275 x 182] intentionally omitted <==**

**==> picture [207 x 194] intentionally omitted <==**

## 

## 

## 

**==> picture [378 x 436] intentionally omitted <==**

**==> picture [368 x 327] intentionally omitted <==**

**==> picture [216 x 236] intentionally omitted <==**

## 

## 

**==> picture [373 x 165] intentionally omitted <==**

**https://t.me/it_boooks/2** 

**==> picture [365 x 162] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

**==> picture [359 x 137] intentionally omitted <==**

## 

## 

**==> picture [334 x 181] intentionally omitted <==**

## 

## 

**==> picture [396 x 294] intentionally omitted <==**

## 

## 

**==> picture [285 x 178] intentionally omitted <==**

## 

## 

## 

## 

## 

**==> picture [372 x 347] intentionally omitted <==**

## 

## 

**==> picture [174 x 204] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [368 x 128] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [370 x 237] intentionally omitted <==**

**==> picture [370 x 255] intentionally omitted <==**

**==> picture [357 x 68] intentionally omitted <==**

**==> picture [348 x 85] intentionally omitted <==**

**==> picture [348 x 84] intentionally omitted <==**

**==> picture [324 x 81] intentionally omitted <==**

**==> picture [348 x 83] intentionally omitted <==**

## 

**==> picture [371 x 139] intentionally omitted <==**

**==> picture [279 x 65] intentionally omitted <==**

**==> picture [169 x 6] intentionally omitted <==**

**==> picture [293 x 83] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

**==> picture [358 x 183] intentionally omitted <==**

## 

**==> picture [373 x 193] intentionally omitted <==**

## 

**==> picture [303 x 215] intentionally omitted <==**

**==> picture [361 x 399] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [289 x 61] intentionally omitted <==**

**==> picture [246 x 139] intentionally omitted <==**

## 

## 

**==> picture [163 x 200] intentionally omitted <==**

## 

## 

## 

**==> picture [304 x 166] intentionally omitted <==**

## 

## 

**==> picture [274 x 196] intentionally omitted <==**

**==> picture [201 x 128] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [94 x 35] intentionally omitted <==**

**==> picture [329 x 283] intentionally omitted <==**

## 

## 

## 

## 

## 

**==> picture [365 x 227] intentionally omitted <==**

## 

## 

**==> picture [358 x 175] intentionally omitted <==**

**==> picture [358 x 345] intentionally omitted <==**

## 

**==> picture [272 x 315] intentionally omitted <==**

## 

## 

**==> picture [350 x 215] intentionally omitted <==**

**==> picture [140 x 62] intentionally omitted <==**

## 

**==> picture [289 x 211] intentionally omitted <==**

**==> picture [307 x 131] intentionally omitted <==**

## 

**==> picture [370 x 176] intentionally omitted <==**

## 

**==> picture [390 x 135] intentionally omitted <==**

## 

**==> picture [238 x 222] intentionally omitted <==**

## 

**==> picture [274 x 302] intentionally omitted <==**

**==> picture [311 x 76] intentionally omitted <==**

## 

## 

**==> picture [215 x 38] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

**==> picture [267 x 57] intentionally omitted <==**

## 

**==> picture [61 x 7] intentionally omitted <==**

**==> picture [104 x 69] intentionally omitted <==**

**==> picture [311 x 86] intentionally omitted <==**

## 

**==> picture [339 x 86] intentionally omitted <==**

**==> picture [253 x 100] intentionally omitted <==**

## 

## 

**==> picture [358 x 298] intentionally omitted <==**

## 

## 

**==> picture [350 x 239] intentionally omitted <==**

## 

## 

## 

**==> picture [268 x 137] intentionally omitted <==**

## 

**==> picture [358 x 212] intentionally omitted <==**

## 

**==> picture [358 x 234] intentionally omitted <==**

**==> picture [359 x 211] intentionally omitted <==**

**==> picture [357 x 181] intentionally omitted <==**

## 

**==> picture [282 x 70] intentionally omitted <==**

## 

**==> picture [372 x 185] intentionally omitted <==**

## 

**==> picture [336 x 106] intentionally omitted <==**

**==> picture [340 x 150] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

**==> picture [357 x 297] intentionally omitted <==**

## 

**==> picture [359 x 189] intentionally omitted <==**

**==> picture [333 x 75] intentionally omitted <==**

## 

**==> picture [353 x 291] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

**==> picture [308 x 363] intentionally omitted <==**

**==> picture [310 x 422] intentionally omitted <==**

## 

**==> picture [372 x 203] intentionally omitted <==**

**==> picture [367 x 136] intentionally omitted <==**

## 

**==> picture [357 x 219] intentionally omitted <==**

**==> picture [322 x 157] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

|||**[Word)**|**[Word!)**|**[Word]!**|**[Word!)!**|
|---|---|---|---|---|---|
|null||Валидно|Валидно|Невалидно|Невалидно|
|[]||Валидно|Валидно|Валидно|Валидно|
|[ "word"]||Валидно|Валидно|Валидно|Валидно|
|[null]||Валидно|Невалидно|Валидно|Невалидно|
|[ "word",null]||Валидно|Невалидно|Валидно|Невалидно|
|Теперь,разобравшисьссистемойтиповGraphQLисвойствами|||||списков,мыгото­|
|выперейти|кизучениюоднойизсамыхмощныхизахватывающихвозможностей|||||
|GraphQL-|связеймеждутипами.|||||



## 

## 

## 

**==> picture [266 x 133] intentionally omitted <==**

**==> picture [284 x 117] intentionally omitted <==**

## 

**==> picture [268 x 171] intentionally omitted <==**

**==> picture [358 x 172] intentionally omitted <==**

## 

|Листинг**8.8.**Представлениеобщихсвойствчерезинтерфейсы<br>interfaceProductinterface{I<br>Обьявnяемтипинтерфейса|Листинг**8.8.**Представлениеобщихсвойствчерезинтерфейсы<br>interfaceProductinterface{I<br>Обьявnяемтипинтерфейса|Листинг**8.8.**Представлениеобщихсвойствчерезинтерфейсы<br>interfaceProductinterface{I<br>Обьявnяемтипинтерфейса|Листинг**8.8.**Представлениеобщихсвойствчерезинтерфейсы<br>interfaceProductinterface{I<br>Обьявnяемтипинтерфейса|Листинг**8.8.**Представлениеобщихсвойствчерезинтерфейсы<br>interfaceProductinterface{I<br>Обьявnяемтипинтерфейса|
|---|---|---|---|---|
|**id:ID**I||Productlnterface|||
|name:Stringl|||||
|price:**Float**|||||
|**ingredients: [IngredientRecipe!]**|||||
|availaЫe:Вooleanl|||||
|**lastUpdated: Datetimel**|||||
|}|||||
|**typeCakeimplements Productinterface**{<br>id:IDI|||1|Тип**Cake**реаnизует<br>интерфейс**Productlnterface**|
|name:Stringl|||||
|price:Float|||||
|availaЫe:Booleanl|||||
|hasFilling:Boolean 1|.......,Опредеnяемсвойства,||||
|hasNutsToppingOption: Boolean|1|1mецифмчные||дnя**Cake**|
|lastUpdated: Datetime!|||||
|ingredients:[IngredientRecipel]!|||||
|}|||||
|**type Beverage implements Productinterface**{ .......,тип**Beverage**реаnизует|||||
|id:ID1||||1интерфейс**Productlnterface**|
|name:Stringl|||||
|price:Float|||||
|availaЫe:Boolean!|||||
|hasCreamOnTopOption: Booleanl|||||
|hasServeOniceOption: Booleanl|||||
|lastUpdated: Datetimel|||||
|ingredients:[IngredientRecipe!]!|||||
|}|||||



## 

**==> picture [265 x 112] intentionally omitted <==**

**==> picture [6 x 9] intentionally omitted <==**

## 

**==> picture [359 x 100] intentionally omitted <==**

## 

**==> picture [108 x 15] intentionally omitted <==**

## 

## 

## 

## 

## 

**==> picture [32 x 12] intentionally omitted <==**

**==> picture [263 x 145] intentionally omitted <==**

**==> picture [362 x 156] intentionally omitted <==**

**==> picture [360 x 117] intentionally omitted <==**

## 

## 

**==> picture [238 x 49] intentionally omitted <==**

**==> picture [260 x 119] intentionally omitted <==**

## 

**==> picture [221 x 48] intentionally omitted <==**

## 

**==> picture [40 x 6] intentionally omitted <==**

**==> picture [277 x 99] intentionally omitted <==**

**==> picture [277 x 88] intentionally omitted <==**

## 

## 

## 

**==> picture [190 x 59] intentionally omitted <==**

**==> picture [327 x 159] intentionally omitted <==**

## 

**==> picture [270 x 69] intentionally omitted <==**

## 

**==> picture [242 x 119] intentionally omitted <==**

**==> picture [242 x 138] intentionally omitted <==**

## 

## 

## 

**==> picture [330 x 176] intentionally omitted <==**

**==> picture [328 x 122] intentionally omitted <==**

## 

**==> picture [351 x 148] intentionally omitted <==**

**==> picture [348 x 326] intentionally omitted <==**

## 

**==> picture [320 x 158] intentionally omitted <==**

## 

**==> picture [369 x 255] intentionally omitted <==**

**==> picture [371 x 303] intentionally omitted <==**

## 

## 

**==> picture [292 x 143] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

**==> picture [359 x 221] intentionally omitted <==**

**==> picture [302 x 311] intentionally omitted <==**

## 

**==> picture [299 x 197] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [359 x 264] intentionally omitted <==**

## 

## 

**==> picture [353 x 360] intentionally omitted <==**

**==> picture [358 x 331] intentionally omitted <==**

## 

**==> picture [367 x 203] intentionally omitted <==**

## 

**==> picture [369 x 238] intentionally omitted <==**

## 

**==> picture [85 x 81] intentionally omitted <==**

**==> picture [120 x 69] intentionally omitted <==**

**==> picture [182 x 168] intentionally omitted <==**

## 

**==> picture [150 x 75] intentionally omitted <==**

## 

## 

**==> picture [309 x 239] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [356 x 138] intentionally omitted <==**

**==> picture [357 x 142] intentionally omitted <==**

**==> picture [6 x 8] intentionally omitted <==**

## 

## 

**==> picture [329 x 49] intentionally omitted <==**

**==> picture [367 x 290] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [369 x 217] intentionally omitted <==**

## 

## 

**==> picture [358 x 324] intentionally omitted <==**

## 

**==> picture [358 x 318] intentionally omitted <==**

## 

**==> picture [321 x 151] intentionally omitted <==**

## 

**==> picture [363 x 153] intentionally omitted <==**

## 

## 

**==> picture [328 x 217] intentionally omitted <==**

## 

## 

**==> picture [201 x 184] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [360 x 250] intentionally omitted <==**

## 

## 

## 

## 

## 

**==> picture [302 x 568] intentionally omitted <==**

## 

## 

## 

## 

## 

**==> picture [354 x 373] intentionally omitted <==**

## 

**==> picture [348 x 74] intentionally omitted <==**

## 

## 

## 

**==> picture [368 x 160] intentionally omitted <==**

## 

## 

**==> picture [357 x 193] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [367 x 257] intentionally omitted <==**

## 

## 

## 

**==> picture [379 x 248] intentionally omitted <==**

**==> picture [306 x 126] intentionally omitted <==**

**==> picture [370 x 214] intentionally omitted <==**

## 

**==> picture [359 x 203] intentionally omitted <==**

**==> picture [347 x 142] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

**==> picture [357 x 162] intentionally omitted <==**

## 

## 

## 

**==> picture [326 x 123] intentionally omitted <==**

## 

**==> picture [285 x 520] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [360 x 358] intentionally omitted <==**

|Performed checks:|||
|---|---|---|
|not_a_server_error|1200 / 1200 passed|PASSED|
|status_code_conformance|1200 / 1200 passed|PASSED|
|content_type_conformance|1200 / 1200 passed|PASSED|
|response_headers_conformance|1200 / 1200 passed|PASSED|
|response_schema_conformance|1200 / 1200 passed|PASSED|



## 

## 

**==> picture [360 x 272] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

**==> picture [301 x 128] intentionally omitted <==**

## 

**==> picture [384 x 179] intentionally omitted <==**

## 

## 

**==> picture [306 x 274] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

## 

**==> picture [358 x 308] intentionally omitted <==**

## 

## 

## 

**==> picture [325 x 223] intentionally omitted <==**

**==> picture [358 x 317] intentionally omitted <==**

## 

|fargate-ip-192-168-173-63.<aws_region>...Ready<br><none><br>4dlбhvl.20.7...|fargate-ip-192-168-173-63.<aws_region>...Ready<br><none><br>4dlбhvl.20.7...|fargate-ip-192-168-173-63.<aws_region>...Ready<br><none><br>4dlбhvl.20.7...|fargate-ip-192-168-173-63.<aws_region>...Ready<br><none><br>4dlбhvl.20.7...|fargate-ip-192-168-173-63.<aws_region>...Ready<br><none><br>4dlбhvl.20.7...|
|---|---|---|---|---|
|Чтобыполучитьсписокмодулей,запущенныхвкластере,выполнитетакуюко­|||||
|манду:|||||
|$kubectlgetpods-А|||||
|NAМESPACE<br>NAME|READY|STATUS|RESTARTS|AGE|
|kube-system coredns-647df9f975-2ns5m|1/1|Running|0|2d15h|
|kube-system coredns-647df9f975-hcgjq|1/1|Running|0|2d15h|



## 

**==> picture [361 x 95] intentionally omitted <==**

## 

## 

**==> picture [369 x 160] intentionally omitted <==**

## 

**==> picture [371 x 177] intentionally omitted <==**

## 

## 

**==> picture [364 x 184] intentionally omitted <==**

**==> picture [349 x 202] intentionally omitted <==**

## 

## 

**==> picture [332 x 124] intentionally omitted <==**

## 

## 

**==> picture [372 x 189] intentionally omitted <==**

## 

## 

**==> picture [360 x 169] intentionally omitted <==**

## 

**==> picture [361 x 141] intentionally omitted <==**

**==> picture [301 x 58] intentionally omitted <==**

## 

## 

## 

## 

**==> picture [375 x 304] intentionally omitted <==**

## 

**==> picture [364 x 272] intentionally omitted <==**

## 

## 

# 

## 

## 

**==> picture [223 x 66] intentionally omitted <==**

**==> picture [371 x 281] intentionally omitted <==**

## 

**==> picture [370 x 241] intentionally omitted <==**

## 

**==> picture [340 x 146] intentionally omitted <==**

**==> picture [265 x 116] intentionally omitted <==**

## 

**==> picture [350 x 483] intentionally omitted <==**

## 

**==> picture [359 x 302] intentionally omitted <==**

**==> picture [300 x 94] intentionally omitted <==**

## 

## 

## 

## 

## 

**==> picture [357 x 506] intentionally omitted <==**

**==> picture [357 x 184] intentionally omitted <==**

## 

## 

**==> picture [379 x 434] intentionally omitted <==**

## 

## 

## 

## 

## 

## 

**==> picture [283 x 311] intentionally omitted <==**

**==> picture [298 x 264] intentionally omitted <==**

## 

**==> picture [403 x 169] intentionally omitted <==**

**==> picture [394 x 231] intentionally omitted <==**

