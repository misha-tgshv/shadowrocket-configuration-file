# Shadowrocket: выборочная защита трафика на iOS и других платформах

Выборочная защита интернет-трафика на iOS, iPadOS, macOS и tvOS с помощью приложения Shadowrocket для пользователей из России. В основе — усовершенствованные правила маршрутизации, позволяющие направлять трафик через прокси-серверы по заданным доменам и портам, обеспечивая удобство и безопасность. Для общения и оперативного обсуждения конфигураций и настроек доступен телеграм-чат [«Про Shadowrocket на русском»](https://t.me/shadowrocket_ru).

## Конфигурации

### Базовый конфиг

Трафик по умолчанию идет напрямую через оператора связи, при этом запросы к доменам из конфигурации направляются через сервер. Так можно пользоваться популярными сервисами без постоянного запуска VPN.

Базовый конфиг [sr_ru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/main/conf/sr_ru_basic.conf) содержит 5 списков:
- `domain_community.list` — домены телеграм-чата «Про Shadowrocket на русском»;
- `domain_refilter.list` — домены сообщества [Re:filter](https://github.com/1andrevich/Re-filter-lists);
- `ip_refilter.list` — IP-адреса сообщества Re:filter;
- `port_discord.list` — порты из списка [@helmiau](https://github.com/helmiau/clashrules/blob/main/shadowrocket/Game_Discord_Ports.list);
- `voice_ports.list` — порты для голосового трафика.

## Модули

Для YouTube доступен модуль [YT-Premium-V1-RU.module](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/modules/YT-Premium-V1-RU.module) с отключенными китайскими субтитрами и необходимыми правилами.

## Обновление списков

Списки обновляются автоматически раз в сутки. Все актуальные файлы находятся в ветке `main`.

- `domain_antifilter.list` — домены сообщества [Антифильтр](https://community.antifilter.download);
- `domain_banking.list` — домены банков из списка ЦБ РФ;
- `domain_youtube.list` — домены из [@blackmatrix7](https://github.com/dsvip/Quantumult-X);
- `domain_discord.list` — домены из [@blackmatrix7](https://github.com/blackmatrix7/ios_rule_script).

## Инструкции и помощь

Подробные инструкции по настройке, использованию и дополнительным функциям доступны в [блоге](https://mishatugushev.ru/blog/?go=all/shadowrocket-seamless).

Поддержать проект можно переводом средств на ЮMoney: [410015839777064](https://yoomoney.ru/to/410015839777064).

## Особенности

- Используются подправила `DOMAIN-SUFFIX` для корректной работы с поддоменами;
- Для популярных доменов (например, Instagram, YouTube) применяется дополнительное подправило `DOMAIN-KEYWORD`;
- Домен `spotify.com` исключен из большинства списков для прямой загрузки контента.
