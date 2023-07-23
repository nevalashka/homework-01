Домашняя работа к уроку с чего начинается linux
Практически все команды взяты из этой методички https://docs.google.com/document/d/12sC884LuLGST3-tZYQBDPvn6AH8AGJCK/edit
Укажу лишь те ошибки, которые исправлял по ходу выполнения задания 
1. Изменил ссылку на образ и хеш сумму для проверки 
"iso_checksum": "029ead89f720becd5ee2a8cf9935aad12fda7494d61674710174b4674b357530",
"iso_url": "http://mirror.linux-ia64.org/centos/8-stream/isos/x86_64/CentOS-Stream-8-20230710.0-x86_64-boot.iso",
2. Параметр "ssh_timeout": "60m",
Сделал для того чтобы образ успел скачаться и выполнились все скрипты в виртуалке
3. "execute_command": "echo 'vagrant'|{{.Vars}} sudo -S -E bash '{{.Path}}'",
Тут благодаря чату в тг изменил строчку для передачи рут пароля. Честно говоря, не понимаю как командой echo можно передать рут пароль.
3.В файле ks.cfg исправил неправильный символ (минус) на 25 строчке   
Выключаем штатный межсетевой экран
firewall --disabled
4. Еще аутификация для вагранта происходит по команде vagrant cloud auth login --token
А не по vagrant cloud auth login





