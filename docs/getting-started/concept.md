# Concept

cBackup использует протоколы SNMP, Telnet и SSH для связи с устройствами и для извлечения данных из узлов. SNMP используется для процессов обнаружения и опроса узлов. Резервное копирование узлов возможно только через протокол Telnet или SSH, однако SNMP предоставляет более подробные данные для управления узлами.

Сам cBackup состоит из двух частей: веб-интерфейса и демона. Веб-интерфейс написан на PHP фреймворке [Yii2 framework](http://www.yiiframework.com), а демон - это приложение Java Spring, работающее в качестве системной службы. Демон общяется с web-ядром cBackup через REST API по протоколу HTTP.

# Ключевые термины

<div id="teminology-table"></div>

_Term_ | _Definition_
------------ | -------------
Узел | Сетевое оборудование, объект конфигурация которого подлежит резервному копированию. Чаще всего **узел** это коммутатор или маршрутизатор различных классов.
Устройство | Класс или группа сетевого оборудования с описанием значений производителя и модели устройства. Для каждого устройства назначается **Шаблон аутентификации**
Authentication template | Sequence of prompts and responses representing authentication sequence for communication via Telnet. Every template can be assigned to any **device**. There're several macros available (e.g. {{telnet_login}}, {{telnet_password}}) representing corresponding data from **credentials**.<br><br><div class="warning">**⚠ Warning!**<br>For communication via SSH all macros will be ignored and initial SSH login and password are retrieved from credentials directly. Rest of the sequence is still used to send privileged mode password if it's required. See [authentiaction documentation](../administrators-guide/authentication) for full information.</div>
Network | Simple subnet of any class, defined in CIDR format. To each subnet particular **credentials** are assigned. 
Credentials | Set of authentication data (logins, passwords, protocols, port numbers, etc) that is used in authentication processes. Credentials set can be assigned to any number of subnets and will be used in numerous cBackup processes.
Discovery | Process of checking nodes in all defined networks. New nodes are discovered, existing are being checked for updates (e.g. if equipment model has been changed) 
Daemon | cBackup main daemon with internal scheduler. Physically it's executable .JAR file. It handles processes of discovery, polling and required configuration data retrieving. Communicates with cBackup web core via REST API.
Schedule | cBackup doesn't rely on system cron and utilizes its' own scheduler. You can schedule system tasks or reporting via email. Each schedule represents one task, so in other words _you schedule a task_.
Task | Particular task itself that could be assigned to nodes or devices. Task consists of **workers**.
Worker | Set of commands intended for specific functionality processing. Primarily worker is described by protocol and consists of **jobs' sequence**
Job | Specific command (Telnet or SSH depending on **worker's** protocol). Also can be SNMP OID if worker, which contains this job works over SNMP protocol. 

# Process components

For process components relations comprehension the following diagram can be used:

![Process elements relations](../assets/processes1.png)
