# Установка Ministra на Ubuntu 20.04 LTS / 18.04 LTS
Скрипт автоматической установки Ministra Portal в Ubuntu 20.04 LTS / 18.04 LTS
# +


Этот скрипт работает только на Clean Ubuntu 20.04 LTS / 18.04 LTS.

Скрипт автоматической установки Ministra

          Версия Ministra 5.6.8

## Установка
```bash
cd /opt
apt-get install git
git clone https://github.com/sybdata/ministra-install-ubuntu-20.04.git
cd /opt/ ministra-install-ubuntu-20.04/
```

Откройте ministra_install_ubuntu.20.04.sh с помощью вашего любимого текстового редактора и внесите изменения в строке 11
```bash
mysql_root_password="123456"
```
Это пароль root для MySQL, который будет установлен во время установки, вы можете изменить его на свой, если хотите.



И в строке 10 измените

```bash
TIME_ZONE="Europe/Moscow"
```
Это часовой пояс, который будет установлен во время установки, вы можете изменить его на свой, если хотите.

Сама установка выглядит следующим образом:

```bash
cd /opt/ministra_install_ubuntu.20.04.sh
./ministra_install_ubuntu.20.04.sh
```
Соответственно, во время установки при выполнении последней команды phing запросит у вас пароль root для MySQL, введите пароль, который вы установили в строке 11



Вы можете получить доступ к своему сталкерскому порталу по адресу: http: // ipadres / stalker_portal. Имя пользователя и пароль для входа на портал являются вашими по умолчанию.

```
Login: admin
pass: 1
```

Удалить все тестовые каналы из базы через терминал

```bash
mysql -u root -p stalker_db
truncate ch_links;
truncate itv;
```


