> ##### Это репозиторий с документацией для cBackup

# cBackup

cBackup [siː ˈbækʌp] — это инструмент резервного копирования конфигурации сетевого оборудования.
# Загрузки

Описание | Дистрибутив | Ссылка на последнюю версию
--------- | --------- | ---------
Стабильный релиз | Archive | [cbackup.tar.gz](http://cbackup.me/latest)
Стабильный релиз | CentOS 7, RPM | [cbackup.el7.noarch.rpm](http://cbackup.me/latest?package=rpm&sub=el7)
Стабильный релиз | CentOS 6, RPM | [cbackup.el6.noarch.rpm](http://cbackup.me/latest?package=rpm&sub=el6)
Стабильный релиз | Ubuntu/Debian, DEB | [cbackup.deb](http://cbackup.me/latest?package=deb)
Бета-версия | Archive | [cbackup_debug-release.tar.gz](http://cbackup.me/latest?package=debug&sub=release)

# Установка

Please refer to [detailed installation description in the official documenation](http://cbackup.readthedocs.io/en/latest/getting-started/install/).

# Essentials and system requirements

cBackup is intended for usage in Linux environment. It consists of two parts: web interface and multithreaded Java daemon. We recommend dedicated standalone appliance due to relatively high demand on resources. Brief system requirements are:
* Linux server
* Web server (Apache, NGinx)
* PHP 7.0 or newer
* Java 8, JRE
* MySQL 5.5 or newer (or compatible MariaDB, Percona, etc)
* Git 1.8 or newer
* NetSNMP
* OpenSSH
* libCurl

# License

Published under the GNU Affero General Public License (AGPLv3)<br>
Copyright 2017 © cBackup Team: Oļegs Čapligins, Imants Černovs, Dmitrijs Galočkins  
