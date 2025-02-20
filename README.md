# Описание
Выборочная защита трафика на iOS, iPadOS, macOS, tvOS через приложение Shadowrocket для пользователей из России. Оперативное обсуждение конфигов, настроек и возможностей в телеграм-чате [«Про Shadowrocket на русском»](https://t.me/shadowrocket_ru). 

## Конфиги
### Базовый конфиг
 Весь трафик будет идти напрямую через вашего оператора связи, а запросы к доменам из конфига будут идти через ваш сервер. Например, у вас будет доступ к Ютуб или Инстаграм без необходимости каждый раз запускать программу для VPN.
Базовый конфиг [sr_ru_public_lists.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/conf/sr_ru_public_lists.conf). Он включает в себя пять списков:
* domain_comunity.list — домены телеграм-чата «Про Shadowrocket на русском»;
* domain_refilter.list — домены из списка сообщества [Re:filter](https://github.com/1andrevich/Re-filter-lists);
* ip_refilter.list — IP-адреса из списка сообщества Re:filer;
* port_discord.list — порты из списка [@helmiau](https://github.com/helmiau/clashrules/blob/main/shadowrocket/Game_Discord_Ports.list)

Все списки, кроме первого, обновляются раз в сутки. Все файлы можно найти в ветке release.

## Модули
Для Youtube можно использовать модуль [YT-Premium-V1-RU.module](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/modules/YT-Premium-V1-RU.module) с отключенными китайскими субтитрами и необходимыми правилами.

## Списки
* domain_antifilter.list — домены из списка сообщества [Антифильтр](https://community.antifilter.download);
* domain_banking.list — домены банков из списка [ЦБ РФ](https://www.cbr.ru/banking_sector/credit/cowebsites/);
* domain_youtube.list — домены из списка [@blackmatrix7](https://raw.githubusercontent.com/dsvip/Quantumult-X/dec9019816ba55897c162c3dbd3ac997ac160f09/blackmatrix7/rule/Shadowrocket/YouTube.list)
* domain_discord.list — домены из списка [@blackmatrix7](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/refs/heads/master/rule/Shadowrocket/Discord/Discord.list)

## Инструкции
Как настроить, пользоваться и подключать разные функции — читайте в [блоге](https://mishatugushev.ru/blog/?go=all/shadowrocket-seamless-ios/).

## Помощь проекту
Поддержать автора можно переводом средств на кошелек [Юмани](https://yoomoney.ru/to/410015839777064).

#### Примечание
* В чем разница между списками с доменами? Если вы подключаете список Антифильтра или Рефильтра напрямую, то там только домены без подправил и с www в начале строки. В своих списках используется подправило DOMAIN-SUFFIX для каждого домена, чтобы в случае появления нового поддомена это не приводило к нарушению роутинга. Чтобы это проверить, подключите Рефильтр и попробуйте зайти на torproject.org. Домен не откроется, трафик будет идти напрямую, так как по-умолчанию в таких списках используется подправило DOMAIN, а не DOMAIN-SUFFIX;
* Для отдельных доменов, таких как instagram или youtube, указывается дополнительное подправило KEYWORD;
* Домен spotify.com удален из списков Антифильтра и Рефильтра, чтобы контент (аудио и изображения) загружались напрямую, кроме главной и авторизации.
