# Shadowrocket: выборочная защита трафика на iOS и других платформах

Выборочная защита интернет-трафика на iOS, iPadOS, macOS и tvOS с помощью приложения Shadowrocket для пользователей из России. В основе — усовершенствованные правила маршрутизации, позволяющие направлять трафик через прокси-серверы по заданным доменам и портам, обеспечивая удобство и безопасность. 

Оперативное обсуждения конфигураций и настроек в телеграм-чате [«Про Shadowrocket на русском»](https://t.me/shadowrocket_ru).

## Генератор конфигов
Настройте под себя [конфиг](http://rocket-conf.ru?ref=github) и скачайте его на устройство. 

## Конфигурации (конфиги)

| Конфиг             | Краткое описание                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| [sr_ru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_basic.conf)  | Базовый конфиг: весь трафик идет напрямую через оператора, кроме доменов из списка, для которых используется прокси. Включает списки сообщества «Про Shadowrocket на русском» и порты голосового трафика.        |
| [sr_ru_geo.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_geo.conf)  | Все в прокси кроме доменов ru/рф, они мимо туннеля. Лучший вариант для звонков Telegram, Whatsapp и Facetime. Подключите дополительно ГЕО базы, ссылки на них есть в 94 строке. Обратите внимание, что может увеличиться время загрузки из Апстора и возможны другими минусы, которые автор пока не обнаружил.|
| [sr_ru_whitelist.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_whitelist.conf)  | БС через провайдера, а остальное в прокси|

## Особенности
- Для популярных доменов (например, Instagram, YouTube) применяется дополнительное подправило `DOMAIN-KEYWORD`;
- Используются подправила `DOMAIN-SUFFIX` для корректной работы с поддоменами и расширяющие возможности, если появился новый поддомен;
- Подключите конфиг [sr_ru_extended.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_extended.conf) и добавьте свои правила, если чего-то нет в списках выше. Удобно, что ничего не слетает после обновления;
- [sr_nonru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_nonru_basic.conf). Конфиг для тех, кто зарубежом, проксирующий все российские домены и домены на кириллице.

## Модули
- Для YouTube доступен модуль [YT-Premium-V1-RU.module](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/modules/YT-Premium-V1-RU.module) с отключенными китайскими субтитрами и необходимыми правилами. Требует выпуск HTTPS-сертификата на устройства. Хорошо работает на iOS, плохо на macOS и не работает на Apple TV.
- Для расшифровки сертификатов используйте модуль [Сertificate](https://github.com/misha-tgshv/shadowrocket-configuration-file/blob/main/modules/Certificate.module). Не придется каждый раз выпускать сертификаты после обновления iOS. Просто создайте один раз сертификат и закиньте в него свои ca-passphrase и ca-p12.

## Актуальные списки
- `domains_community.list` — домены сообщества «Про Shadowrocket на русском», включающие универсальные правила для популярных доменов;
- `banking.list` — список доменов банков и финсервисов с сайта ЦБ РФ;
- `domains_ipchecker` - чекеры, использующиеся в российских приложения.

## Где брать еще списки?
- Использовать популярные от Blackmatrix7. Например, для [ТГ](https://github.com/blackmatrix7/ios_rule_script/refs/heads/master/rule/Shadowrocket/Telegram/Telegram.list);
- Поискать актуальные в разных форматах на [IPlist](https://iplist.opencck.org/ru/). Для SR подойдет формате в Text;

## Инструкции и помощь
Подробные инструкции по настройке, использованию и дополнительным функциям доступны в [блоге](https://mishatugushev.ru/blog/?go=all/shadowrocket-seamless). Поддержать проект можно на [Бусти](https://boosty.to/misha_tgshv/donate).
