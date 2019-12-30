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

# Системные требования

cBackup предназначен для использования в среде Linux. Он состоит из двух частей: веб-интерфейс и мультипотоковый Java-демон. Мы рекомендуем использовать отдельный сервер (виртуальная машина или физический) из-за высокого спроса на ресурсы. 
<br>Системные требования:
* Linux-сервер (CentOS 6,7 или Debian/Ubuntu)
* Веб-сервер (Apache, NGinx)
* PHP 7.0 или новее
* Java 8, JRE
* MySQL 5.5 или новее (или совместимые MariaDB, Percona и т.д)
* Git 1.8 или новее
* NetSNMP
* OpenSSH
* libCurl

# Лицензия

Опубликовано под GNU Affero General Public License (AGPLv3)<br>
Copyright 2017 © cBackup Team: Oļegs Čapligins, Imants Černovs, Dmitrijs Galočkins
<br>Перевел на русский язык [Linux-boss](https://github.com/Linux-boss). Перевод опубликован на сайте [Network Lion](https://network-lion.ru/)
