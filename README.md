# TEST
## _Installing Grafana in Docker via Ansible_

Данный playbook разворачивает Grafana с PostgresSQL и и настраивает проксирование к сайту через NGINX.
### Используемое ПО  
- Ansible
- Nginx
- Docker
- Grafana
- PostgreSQL

В качестве хостовой ОС используется Ubuntu 22.04

## Порядок установки

Установим Ansible:
```sh
sudo apt install -y ansible
```
После клонирования прокета переходим в директорию проекта и уставливаем роли из файла requirements.yml:
```
ansible-galaxy install -r requirements.yml
```

Измените значения в файлах _inventory_ и _group vars на свои_. Переменная _server_name_ используется для конфига NGINX.

Запуск Ansible
```
ansible-playbook playbook.yml
```
После раскатки данного плейбука Grafana будет доступна по 80 порту.
