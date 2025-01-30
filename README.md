Ansible playbooks
to run:
ansible-playbook haproxy_config.yml --syntax-check

ansible-playbook -i hosts haproxy_config.yml

Если хотите предварительно проверить, что всё настроено правильно, добавьте флаг --check для запуска в тестовом режиме (без реальных изменений):
<bash>
ansible-playbook -i hosts angie_config.yml --limit 192.168.1.81 --check
</bash>
