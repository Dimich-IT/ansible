># Описание чего здесь вообще и для чего

> Дерево файлов должно быть следующего вида:
```
playbooks/
├── angie_config.yml
└── Angie_config_files/
    ├── angie.conf
    └── http.d/
        ├── file1.conf
        ├── file2.conf
```

>## Ansible playbooks to run: 

>**Если хотим проверить** 
```
ansible-playbook haproxy_config.yml --syntax-check
```

>**Боевой запуск**
```
ansible-playbook -i hosts haproxy_config.yml
```
>Если хотите предварительно проверить, что всё настроено правильно, добавьте флаг --check для запуска в тестовом режиме (без реальных изменений): 
```
ansible-playbook -i hosts angie_config.yml --limit 192.168.1.81 --check
```
>Если нужно больше деталей в выводе, добавьте -v (или -vvv для отладочной информации):
```
ansible-playbook -i hosts angie_config.yml --limit 192.168.1.81 -v
```

>Для выполнения Ansible Playbook на одном конкретном хосте вы можете использовать параметр --limit, чтобы указать имя или IP-адрес целевого хоста. Вот пример команды:

Пример команды:

```ansible-playbook -i hosts angie_config.yml --limit 192.168.1.81
```
