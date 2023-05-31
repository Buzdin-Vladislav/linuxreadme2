vlad@vlad-VirtualBox:~$ 
vlad@vlad-VirtualBox:~$ echo "deb http://nginx.org/packages/ubuntu focal nginx" > nginx.list
vlad@vlad-VirtualBox:~$ cur1 -fsSl https://nginx.org/keys/nginx_signing.key | sudo apt-key add - 
[sudo] пароль для vlad: Команда «cur1» не найдена. Возможно, вы имели в виду:
  command 'curl' from deb curl (7.81.0-1ubuntu1.10)
  command 'cura' from deb cura (4.13.0-1)
Try: sudo apt install <deb name>

Попробуйте ещё раз.
[sudo] пароль для vlad: 
Попробуйте ещё раз.
[sudo] пароль для vlad: 
Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
gpg: не найдено данных формата OpenPGP.
vlad@vlad-VirtualBox:~$ curl -fsSl https://nginx.org/keys/nginx_signing.key | sudo apt-key add - 
Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
Команда «curl» не найдена, но может быть установлена с помощью:
sudo apt install curl
gpg: не найдено данных формата OpenPGP.
vlad@vlad-VirtualBox:~$ sudo apt update
Сущ:1 http://ru.archive.ubuntu.com/ubuntu jammy InRelease
Пол:2 http://ru.archive.ubuntu.com/ubuntu jammy-updates InRelease [119 kB]
Пол:3 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]   
Пол:4 http://ru.archive.ubuntu.com/ubuntu jammy-backports InRelease [108 kB]
Пол:5 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 Packages [657 kB]
Пол:6 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main i386 Packages [409 kB]
Пол:7 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main Translation-en [179 kB]
Пол:8 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 DEP-11 Metadata [101 kB]
Пол:9 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 c-n-f Metadata [14,7 kB]
Пол:10 http://ru.archive.ubuntu.com/ubuntu jammy-updates/restricted amd64 Packages [341 kB]
Пол:11 http://ru.archive.ubuntu.com/ubuntu jammy-updates/restricted Translation-en [51,4 kB]
Пол:12 http://ru.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 Packages [906 kB]
Пол:13 http://ru.archive.ubuntu.com/ubuntu jammy-updates/universe i386 Packages [616 kB]
Пол:14 http://ru.archive.ubuntu.com/ubuntu jammy-updates/universe Translation-en [187 kB]
Пол:15 http://ru.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 DEP-11 Metadata [269 kB]
Пол:16 http://ru.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 c-n-f Metadata [19,5 kB]
Пол:17 http://ru.archive.ubuntu.com/ubuntu jammy-updates/multiverse amd64 DEP-11 Metadata [940 B]
Пол:18 http://ru.archive.ubuntu.com/ubuntu jammy-backports/main amd64 DEP-11 Metadata [7 976 B]
Пол:19 http://ru.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 DEP-11 Metadata [16,9 kB]
Пол:20 http://ru.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 c-n-f Metadata [548 B]
Пол:21 http://security.ubuntu.com/ubuntu jammy-security/main amd64 Packages [405 kB]
Пол:22 http://security.ubuntu.com/ubuntu jammy-security/main i386 Packages [220 kB]
Пол:23 http://security.ubuntu.com/ubuntu jammy-security/main Translation-en [115 kB]
Пол:24 http://security.ubuntu.com/ubuntu jammy-security/main amd64 DEP-11 Metadata [41,6 kB]
Пол:25 http://security.ubuntu.com/ubuntu jammy-security/main amd64 c-n-f Metadata [9 908 B]
Пол:26 http://security.ubuntu.com/ubuntu jammy-security/restricted amd64 Packages [279 kB]
Пол:27 http://security.ubuntu.com/ubuntu jammy-security/restricted Translation-en [40,8 kB]
Пол:28 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 Packages [724 kB]
Пол:29 http://security.ubuntu.com/ubuntu jammy-security/universe i386 Packages [532 kB]
Пол:30 http://security.ubuntu.com/ubuntu jammy-security/universe Translation-en [127 kB]
Пол:31 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 DEP-11 Metadata [19,1 kB]
Пол:32 http://security.ubuntu.com/ubuntu jammy-security/universe DEP-11 48x48 Icons [16,5 kB]
Пол:33 http://security.ubuntu.com/ubuntu jammy-security/universe DEP-11 64x64 Icons [26,3 kB]
Пол:34 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 c-n-f Metadata [15,2 kB]
Получено 6 686 kB за 4с (1 807 kB/s)                                         
 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Может быть обновлено 178 пакетов. Запустите «apt list --upgradable» для их показа.
vlad@vlad-VirtualBox:~$ sudo apt install nginx -y
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Будут установлены следующие дополнительные пакеты:
  libnginx-mod-http-geoip2 libnginx-mod-http-image-filter
  libnginx-mod-http-xslt-filter libnginx-mod-mail libnginx-mod-stream
  libnginx-mod-stream-geoip2 nginx-common nginx-core
Предлагаемые пакеты:
  fcgiwrap nginx-doc
Следующие НОВЫЕ пакеты будут установлены:
  libnginx-mod-http-geoip2 libnginx-mod-http-image-filter
  libnginx-mod-http-xslt-filter libnginx-mod-mail libnginx-mod-stream
  libnginx-mod-stream-geoip2 nginx nginx-common nginx-core
Обновлено 0 пакетов, установлено 9 новых пакетов, для удаления отмечено 0 пакетов, и 178 пакетов не обновлено.
Необходимо скачать 696 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 2 395 kB.
Пол:1 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 nginx-common all 1.18.0-6ubuntu14.3 [40,0 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnginx-mod-http-geoip2 amd64 1.18.0-6ubuntu14.3 [11,9 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnginx-mod-http-image-filter amd64 1.18.0-6ubuntu14.3 [15,4 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnginx-mod-http-xslt-filter amd64 1.18.0-6ubuntu14.3 [13,7 kB]
Пол:5 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnginx-mod-mail amd64 1.18.0-6ubuntu14.3 [45,7 kB]
Пол:6 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnginx-mod-stream amd64 1.18.0-6ubuntu14.3 [72,8 kB]
Пол:7 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnginx-mod-stream-geoip2 amd64 1.18.0-6ubuntu14.3 [10,1 kB]
Пол:8 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 nginx-core amd64 1.18.0-6ubuntu14.3 [482 kB]
Пол:9 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 nginx amd64 1.18.0-6ubuntu14.3 [3 882 B]
Получено 696 kB за 0с (1 471 kB/s)         
Предварительная настройка пакетов …
Выбор ранее не выбранного пакета nginx-common.
(Чтение базы данных … на данный момент установлено 205480 файлов и каталогов.)
Подготовка к распаковке …/0-nginx-common_1.18.0-6ubuntu14.3_all.deb …
Распаковывается nginx-common (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета libnginx-mod-http-geoip2.
Подготовка к распаковке …/1-libnginx-mod-http-geoip2_1.18.0-6ubuntu14.3_amd64.d
eb …
Распаковывается libnginx-mod-http-geoip2 (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета libnginx-mod-http-image-filter.
Подготовка к распаковке …/2-libnginx-mod-http-image-filter_1.18.0-6ubuntu14.3_a
md64.deb …
Распаковывается libnginx-mod-http-image-filter (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета libnginx-mod-http-xslt-filter.
Подготовка к распаковке …/3-libnginx-mod-http-xslt-filter_1.18.0-6ubuntu14.3_am
d64.deb …
Распаковывается libnginx-mod-http-xslt-filter (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета libnginx-mod-mail.
Подготовка к распаковке …/4-libnginx-mod-mail_1.18.0-6ubuntu14.3_amd64.deb …
Распаковывается libnginx-mod-mail (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета libnginx-mod-stream.
Подготовка к распаковке …/5-libnginx-mod-stream_1.18.0-6ubuntu14.3_amd64.deb …
Распаковывается libnginx-mod-stream (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета libnginx-mod-stream-geoip2.
Подготовка к распаковке …/6-libnginx-mod-stream-geoip2_1.18.0-6ubuntu14.3_amd64
.deb …
Распаковывается libnginx-mod-stream-geoip2 (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета nginx-core.
Подготовка к распаковке …/7-nginx-core_1.18.0-6ubuntu14.3_amd64.deb …
Распаковывается nginx-core (1.18.0-6ubuntu14.3) …
Выбор ранее не выбранного пакета nginx.
Подготовка к распаковке …/8-nginx_1.18.0-6ubuntu14.3_amd64.deb …
Распаковывается nginx (1.18.0-6ubuntu14.3) …
Настраивается пакет nginx-common (1.18.0-6ubuntu14.3) …
Created symlink /etc/systemd/system/multi-user.target.wants/nginx.service → /li
b/systemd/system/nginx.service.
Настраивается пакет libnginx-mod-http-xslt-filter (1.18.0-6ubuntu14.3) …
Настраивается пакет libnginx-mod-http-geoip2 (1.18.0-6ubuntu14.3) …
Настраивается пакет libnginx-mod-mail (1.18.0-6ubuntu14.3) …
Настраивается пакет libnginx-mod-http-image-filter (1.18.0-6ubuntu14.3) …
Настраивается пакет libnginx-mod-stream (1.18.0-6ubuntu14.3) …
Настраивается пакет libnginx-mod-stream-geoip2 (1.18.0-6ubuntu14.3) …
Настраивается пакет nginx-core (1.18.0-6ubuntu14.3) …
 * Upgrading binary nginx                                               [ OK ] 
Настраивается пакет nginx (1.18.0-6ubuntu14.3) …
Обрабатываются триггеры для man-db (2.10.2-1) …
Обрабатываются триггеры для ufw (0.36.1-4build1) …
vlad@vlad-VirtualBox:~$ sudo snap install robomongo
robomongo 0.9.0-rc9 от Francesco Banconi (frankban) установлен
vlad@vlad-VirtualBox:~$ 
