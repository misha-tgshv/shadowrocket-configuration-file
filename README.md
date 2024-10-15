Выборочная защита трафика на iOS, iPadOS, macOS через Shadowrocket. Весь трафик будет идти напрямую через провайдера, а домены из конфига будут идти через ваш сервер. Описание работы программы описано в [посте](https://mishatugushev.ru/blog/?go=all/shadowrocket-seamless-ios/).

Основой конфиг [sr_ru_public_lists.conf](https://cdn.jsdelivr.net/gh/misha-tgshv/shadowrocket-configuration-file@release/conf/sr_ru_public_lists.conf). Он включает в себя три списка:
* domain_custom.list — домены на усмотрение автора;
* domain_antifilter.list — домены из списка сообщества [антифильтр](https://community.antifilter.download);
* geoip_antifilter.list — IP-адреса из списка сообщества антифильтр.

Последние два списка обновляются ежедневно. Все файлы можно найти в ветке release.
