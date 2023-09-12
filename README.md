# Урок 2. Механизмы контрольных групп
Задание 1:
1) запустить контейнер с ubuntu, используя механизм LXC
2) ограничить контейнер 256 Мб ОЗУ и проверить, что ограничение работает


Установка LXC с помощью команды:

sudo apt install lxc lxc-templates uidmap

Инициализация LXC:

lxd init

Проверка установленной версии:

lxc version

![Screen1](https://github.com/SokolikAA/container2/assets/115178275/5fc11394-8814-4a3a-aa88-c703805d869c)

Cоздание нового контейнера с именем homeWork2 и с указанием пути для файла конфигурации с помощью команды:

lxc-create -n homeWork2 -t ubuntu -f /usr/share/doc/liblxc-common/examples/lxc-veth.conf

![Screen2](https://github.com/SokolikAA/container2/assets/115178275/a7f8154f-42b3-46aa-bb0d-7cc56cf8813d)


Запуск созданного контейнера:

sudo lxc-start -d -n homeWork2

