# Elastic Stack

### Развертывание Elastic Stack с помощью Ansible & Roles
### Сбор логов Nginx

#### Развертывание происходит на одной ВМ. Все сервисы слушают на localhost.
#### Перед развертыванием добавить на ВМ ssh-ключи пользователя, от которого будет запускаться Ansible. 
#### Запускать из корневого каталога (где ansible.cfg)

#### До запуска, добавить в hosts.ini адрес хоста развертывания:

#### [nginx_srv]
#### nginx ansible_host= <HOST_IP>

### Установка:
#### ansible-playbook install_nginx.yaml
#### ansible-playbook install_elk.yaml

### Подключение:

#### # nginx
#### ssh ansible@nginx -L 5580:localhost:80
#### http://localhost:5580/

#### # Kibana
#### ssh ansible@nginx -L 5601:localhost:5601
#### http://localhost:5601
