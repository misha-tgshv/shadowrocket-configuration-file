# Shadowrocket: выборочная защита трафика на iOS и других платформах

Выборочная защита интернет-трафика на iOS, iPadOS, macOS и tvOS с помощью приложения Shadowrocket для пользователей из России. В основе — усовершенствованные правила маршрутизации, позволяющие направлять трафик через прокси-серверы по заданным доменам и портам, обеспечивая удобство и безопасность. Оперативное обсуждения конфигураций и настроек в телеграм-чате [«Про Shadowrocket на русском»](https://t.me/shadowrocket_ru).


## Конфигурации (конфиги)

| Конфиг             | Краткое описание                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| [sr_ru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_basic.conf)  | Базовый конфиг: весь трафик идет напрямую через оператора, кроме доменов из списка, для которых используется прокси. Включает списки сообщества «Про Shadowrocket на русском» и порты голосового трафика.        |
| [sr_ru_geo.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_geo.conf)  | Все в прокси кроме доменов ru/рф, они мимо туннеля. Лучший вариант для звонков Telegram, Whatsapp и Facetime. Подключите дополительно ГЕО базы, ссылки на них есть в 94 строке. Обратите внимание, что может увеличиться время загрузки из Апстора и возможны другими минусы, которые автор пока не обнаружил.|
| [sr_ru_mini.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_mini.conf)   | Минимальный конфиг с ограниченным числом популярных проксированных доменов для быстрой и легкой настройки.    |
| [sr_ru_extended.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_extended.conf) | Расширенный конфиг с возможностью добавлять собственные правила маршрутизации. Можно не скачивать, а создать в приложении.                              |
| [sr_nonru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_nonru_basic.conf) | Конфиг для тех, кто зарубежом, проксирующий все российские домены и домены на кириллице.

## Особенности конфигов
- Для популярных доменов (например, Instagram, YouTube) применяется дополнительное подправило `DOMAIN-KEYWORD`;
- Используются подправила `DOMAIN-SUFFIX` для корректной работы с поддоменами и расширяющие возможности, если появился новый поддомен;

## Модули
Для YouTube доступен модуль [YT-Premium-V1-RU.module](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/modules/YT-Premium-V1-RU.module) с отключенными китайскими субтитрами и необходимыми правилами. Требует выпуск HTTPS-сертификата на устройства. Хорошо работает на iOS, плохо на macOS и не работает на Apple TV.

## Актуальные списки
- `domains_community.list` — домены сообщества «Про Shadowrocket на русском», включающие универсальные правила для популярных доменов;
- `voice_ports.list` — порты для работы аудиозвонков в Whatsapp и Telegram;
- `Telegram.list` — универсальный список, включающий в себя правила по доменам и диапазону IP-адресов от [@blackmatrix7](https://github.com/blackmatrix7/ios_rule_script/refs/heads/master/rule/Shadowrocket/Telegram/Telegram.list);

## Исключенные списки
Из-за некорректной обработки или каких-то других причин в списки постоянно попадают самые обыкновенные домены или IP-адреса от Яндекса, Google и т.д. Поэтому с 30 августа 2025 было решено их исключить из конфигов. Вы можете ими пользоваться на свой страх и риск. Они будут попрежнему обновляться:
- `domains_refilter.list` — домены сообщества [Антифильтр](https://community.antifilter.download);
- `ips_refilter.list` — ip-адреса сообщества [Антифильтр](https://community.antifilter.download);
- `domain_antifilter.list` — домены сообщества [Антифильтр](https://community.antifilter.download);

## Рекомендованные списки
- `whatsapp_cidr_ipv4.list` — список от @HybridNetworks, который имеет наибольший, актуальный, обновляющийся список ip-адресов Whatsapp;
- `inside-raw.lst` — домены от [@itdog](https://github.com/itdoginfo/allow-domains/blob/main/Russia/inside-clashx.lst);
- `domain_youtube.list` — домены для Ютуба из [@blackmatrix7](https://github.com/dsvip/Quantumult-X);
- `domain_discord.list` — домены для Дискорда из [@blackmatrix7](https://github.com/blackmatrix7/ios_rule_script).

## Инструкции и помощь
Подробные инструкции по настройке, использованию и дополнительным функциям доступны в [блоге](https://mishatugushev.ru/blog/?go=all/shadowrocket-seamless).
Поддержать проект можно переводом средств на ЮMoney: [410015839777064](https://yoomoney.ru/to/410015839777064).
