# Описание проекта
Выборочная защита трафика на iOS, iPadOS, macOS, tvOS через Shadowrocket для пользователей из России. Весь трафик будет идти напрямую через вашего оператора связи, а запросы к доменам из конфига будут идти через ваш сервер. Например, у вас будет доступ к Ютуб или Инстаграм без необходимости каждый раз запускать программу для VPN.

Основой конфиг [sr_ru_public_lists.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/conf/sr_ru_public_lists.conf). Он включает в себя шесть списков:
* domain_custom.list — домены на усмотрение автора;
* domain_antifilter.list — домены из списка сообщества [антифильтр](https://community.antifilter.download);
* domain_refilter.list — домены из списка сообщества [re-filter](https://github.com/1andrevich/Re-filter-lists);
* geoip_antifilter.list — IP-адреса из списка сообщества антифильтр;
* domain_youtube.list — домены из списка [@blackmatrix7](https://raw.githubusercontent.com/dsvip/Quantumult-X/dec9019816ba55897c162c3dbd3ac997ac160f09/blackmatrix7/rule/Shadowrocket/YouTube.list)
* domain_discord.list — домены из списка [@blackmatrix7](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/refs/heads/master/rule/Shadowrocket/Discord/Discord.list)

Все списки кроме первого обновляются ежедневно. Все файлы можно найти в ветке release.

## Инструкции
Как настроить, как пользоваться и подключать разные функции читайте в [блоге](https://mishatugushev.ru/blog/?go=all/shadowrocket-seamless-ios/).

## Помощь проекту
Поддержать автора для добавления новых инструкций, улучшение и обновление конфигов можно переводом средств на кошелек [Юмани](https://yoomoney.ru/to/410015839777064).
