# Домашнее задание к занятию "`Система мониторинга Zabbix. Часть 2`" - `Хорошев Леонид`

---

### Задание 1. Установите Zabbix Server с веб-интерфейсом

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix1.png)
---

### Задание 2 Добавьте в Zabbix два хоста и задайте им имена <фамилия и инициалы-1> и <фамилия и инициалы-2>.

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix2.png)
---


### Задание 4. Создайте свой кастомный дашборд.

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix3.png)
---


### Задание 5. Создайте карту и расположите на ней два своих хоста

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix4.1.png)

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix4.2.png)
---


### Задание 6. Создайте UserParameter на bash и прикрепите его к созданному вами ранее шаблону. Он должен вызывать скрипт, который:

при получении 1 будет возвращать ваши ФИО,

при получении 2 будет возвращать текущую дату.

Код скрипта:

#!/bin/bash

read a

if [[ "$a" -eq 1 ]]; then

    echo "Khoroshev Leonid"

elif [[ "$a" -eq 2 ]]; then

    echo $(date '+%Y-%m-%d')

else

    echo "I don't know what is it"

fi


Результат работы скрипта при вводе параметра 1

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix5.2.png)


Результат работы скрипта при вводе параметра 2

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix5.1.png)
---


### Задание 7. Доработайте Python-скрипт из лекции, создайте для него UserParameter и прикрепите его к созданному вами ранее шаблону. Скрипт должен:

при получении 1 будет возвращать ваши ФИО,

при получении 2 будет возвращать текущую дату.

Код скрипта:

import sys

import datetime

if (sys.argv[1] == "1"):
    
    print("Khoroshev Leonid")
    
elif (sys.argv[1] == "2"):

    print(datetime.datetime.now().strftime("%Y-%m-%d %H:%M"))

else:
    print("I don't khow what is it")

Результат работы скрипта при вводе параметра 1

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix6.1.png)

Результат работы скрипта при вводе параметра 2

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix6.2.png)
---


### Задание 8. Настройте автообнаружение и прикрепление к хостам созданного вами ранее шаблона.

Скриншот правила обнаружения

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix7.1.png)

Скриншот страницы Discover

![alt text](https://github.com/LeonidKhoroshev/hw-08-03/blob/main/zabbix7.2.png)

