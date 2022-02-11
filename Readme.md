curl -s -k -X GET https://api.telegram.org/bot<api_bot>/getUpdates | grep -oE "\"id\":[[:digit:]]+" | head -n1 | awk -F : '{print $2}'

chmod +x -R /usr/lib/telegramopenwrt/plugins/* /usr/lib/telegramopenwrt/plugins/actions/*
chmod +x /etc/init.d/*
chmod +x /etc/config/*
chmod +x /etc/telegramopenwrt/*
chmod +x /sbin/*

/etc/init.d/lanports enable
/etc/init.d/telegram_bot enable
/etc/init.d/lanports start
/etc/init.d/telegram_bot start



Script By Aryo Brokolly

