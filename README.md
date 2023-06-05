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
vlad@vlad-VirtualBox:~$ sudo apt install apache2
[sudo] пароль для vlad: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Следующие пакеты устанавливались автоматически и больше не требуются:
  linux-headers-5.19.0-32-generic linux-hwe-5.19-headers-5.19.0-32
  linux-image-5.19.0-32-generic linux-modules-5.19.0-32-generic
  linux-modules-extra-5.19.0-32-generic
Для их удаления используйте «sudo apt autoremove».
Будут установлены следующие дополнительные пакеты:
  apache2-bin apache2-data apache2-utils libapr1 libaprutil1
  libaprutil1-dbd-sqlite3 libaprutil1-ldap
Предлагаемые пакеты:
  apache2-doc apache2-suexec-pristine | apache2-suexec-custom www-browser
Следующие НОВЫЕ пакеты будут установлены:
  apache2 apache2-bin apache2-data apache2-utils libapr1 libaprutil1
  libaprutil1-dbd-sqlite3 libaprutil1-ldap
Обновлено 0 пакетов, установлено 8 новых пакетов, для удаления отмечено 0 пакетов, и 0 пакетов не обновлено.
Необходимо скачать 1 917 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 7 706 kB.
Хотите продолжить? [Д/н] Д
Пол:1 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libapr1 amd64 1.7.0-8ubuntu0.22.04.1 [108 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libaprutil1 amd64 1.6.1-5ubuntu4.22.04.1 [92,6 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libaprutil1-dbd-sqlite3 amd64 1.6.1-5ubuntu4.22.04.1 [11,3 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 libaprutil1-ldap amd64 1.6.1-5ubuntu4.22.04.1 [9 168 B]
Пол:5 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2-bin amd64 2.4.52-1ubuntu4.5 [1 345 kB]
Пол:6 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2-data all 2.4.52-1ubuntu4.5 [165 kB]
Пол:7 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2-utils amd64 2.4.52-1ubuntu4.5 [89,1 kB]
Пол:8 http://ru.archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2 amd64 2.4.52-1ubuntu4.5 [97,8 kB]
Получено 1 917 kB за 7с (269 kB/s)                                            
Выбор ранее не выбранного пакета libapr1:amd64.
(Чтение базы данных … на данный момент установлено 242004 файла и каталога.)
Подготовка к распаковке …/0-libapr1_1.7.0-8ubuntu0.22.04.1_amd64.deb …
Распаковывается libapr1:amd64 (1.7.0-8ubuntu0.22.04.1) …
Выбор ранее не выбранного пакета libaprutil1:amd64.
Подготовка к распаковке …/1-libaprutil1_1.6.1-5ubuntu4.22.04.1_amd64.deb …
Распаковывается libaprutil1:amd64 (1.6.1-5ubuntu4.22.04.1) …
Выбор ранее не выбранного пакета libaprutil1-dbd-sqlite3:amd64.
Подготовка к распаковке …/2-libaprutil1-dbd-sqlite3_1.6.1-5ubuntu4.22.04.1_amd6
4.deb …
Распаковывается libaprutil1-dbd-sqlite3:amd64 (1.6.1-5ubuntu4.22.04.1) …
Выбор ранее не выбранного пакета libaprutil1-ldap:amd64.
Подготовка к распаковке …/3-libaprutil1-ldap_1.6.1-5ubuntu4.22.04.1_amd64.deb …
Распаковывается libaprutil1-ldap:amd64 (1.6.1-5ubuntu4.22.04.1) …
Выбор ранее не выбранного пакета apache2-bin.
Подготовка к распаковке …/4-apache2-bin_2.4.52-1ubuntu4.5_amd64.deb …
Распаковывается apache2-bin (2.4.52-1ubuntu4.5) …
Выбор ранее не выбранного пакета apache2-data.
Подготовка к распаковке …/5-apache2-data_2.4.52-1ubuntu4.5_all.deb …
Распаковывается apache2-data (2.4.52-1ubuntu4.5) …
Выбор ранее не выбранного пакета apache2-utils.
Подготовка к распаковке …/6-apache2-utils_2.4.52-1ubuntu4.5_amd64.deb …
Распаковывается apache2-utils (2.4.52-1ubuntu4.5) …
Выбор ранее не выбранного пакета apache2.
Подготовка к распаковке …/7-apache2_2.4.52-1ubuntu4.5_amd64.deb …
Распаковывается apache2 (2.4.52-1ubuntu4.5) …
Настраивается пакет libapr1:amd64 (1.7.0-8ubuntu0.22.04.1) …
Настраивается пакет apache2-data (2.4.52-1ubuntu4.5) …
Настраивается пакет libaprutil1:amd64 (1.6.1-5ubuntu4.22.04.1) …
Настраивается пакет libaprutil1-ldap:amd64 (1.6.1-5ubuntu4.22.04.1) …
Настраивается пакет libaprutil1-dbd-sqlite3:amd64 (1.6.1-5ubuntu4.22.04.1) …
Настраивается пакет apache2-utils (2.4.52-1ubuntu4.5) …
Настраивается пакет apache2-bin (2.4.52-1ubuntu4.5) …
Настраивается пакет apache2 (2.4.52-1ubuntu4.5) …
Enabling module mpm_event.
Enabling module authz_core.
Enabling module authz_host.
Enabling module authn_core.
Enabling module auth_basic.
Enabling module access_compat.
Enabling module authn_file.
Enabling module authz_user.
Enabling module alias.
Enabling module dir.
Enabling module autoindex.
Enabling module env.
Enabling module mime.
Enabling module negotiation.
Enabling module setenvif.
Enabling module filter.
Enabling module deflate.
Enabling module status.
Enabling module reqtimeout.
Enabling conf charset.
Enabling conf localized-error-pages.
Enabling conf other-vhosts-access-log.
Enabling conf security.
Enabling conf serve-cgi-bin.
Enabling site 000-default.
Created symlink /etc/systemd/system/multi-user.target.wants/apache2.service → /
lib/systemd/system/apache2.service.
Could not execute systemctl:  at /usr/bin/deb-systemd-invoke line 142.
Created symlink /etc/systemd/system/multi-user.target.wants/apache-htcacheclean
.service → /lib/systemd/system/apache-htcacheclean.service.
Обрабатываются триггеры для ufw (0.36.1-4build1) …
Обрабатываются триггеры для man-db (2.10.2-1) …
Обрабатываются триггеры для libc-bin (2.35-0ubuntu3.1) …
vlad@vlad-VirtualBox:~$ 
  vlad@vlad-VirtualBox:~$ sudo systemctl enable apache2
Synchronizing state of apache2.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable apache2
 If you just change the port or add more ports here, you will likely also
# have to change the VirtualHost statement in
# /etc/apache2/sites-enabled/000-default.conf
vlad@vlad-VirtualBox:~$ sudo nano /etc/apache2/ports.conf


Listen 80

<IfModule ssl_module>
        Listen 8888
</IfModule>

<IfModule mod_gnutls.c>
        Listen 8888
</IfModule>

# vim: syntax=apache ts=4 sw=4 sts=4 sr noet

vlad@vlad-VirtualBox:~$ sudo apt install libapache2-mod-php8.1
server {
listen 80 default_server;
listen [::]:80 default-html;

root /var/www/html;

index index.html index.htm index.nginx-debian.html;

server_name _;

location / {
proxy_pass http://localhost:8888;
proxy_set_header Host Shost;
proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
proxy_set_header X-Real-IP Sremote-addr;
}

location ~* ^.+.(jpg|jpeg|gif|png|ico|css|zip|pdf|txt|tar|js|)$ {root /var/www>
}
}
vlad@vlad-VirtualBox:~$ sudo apt update

vlad@vlad-VirtualBox:~$ sudo apt install mysql-server mysql-client
  vlad@vlad-VirtualBox:~$ sudo dpkg -i ~/Загрузки/mysql-apt-config
vlad@vlad-VirtualBox:~$ sudo apt update
vlad@vlad-VirtualBox:~$ sudo apt install mysql-server mysql-client


