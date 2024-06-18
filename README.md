# Домашнее задание к занятию 1 «Введение в Ansible»

### Основная часть
### Попробуйте запустить playbook на окружении из test.yml, зафиксируйте значение, которое имеет факт some_fact для указанного хоста при выполнении playbook.
1. Запустили. Зафиксировали.
### ![](https://github.com/Berezhok/ansible_one/blob/main/img/playbookUp.png) 
### Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на all default fact.
1. Поменяли, вместо 12 стало all default fact.
### Воспользуйтесь подготовленным (используется docker) или создайте собственное окружение для проведения дальнейших испытаний.
1. Подняли 2 контейнера с помощью docker. 
### Проведите запуск playbook на окружении из prod.yml. Зафиксируйте полученные значения some_fact для каждого из managed host.
### ![](https://github.com/Berezhok/ansible_one/blob/main/img/docker.png) 
### Добавьте факты в group_vars каждой из групп хостов так, чтобы для some_fact получились значения: для deb — deb default fact, для el — el default fact.
### Повторите запуск playbook на окружении prod.yml. Убедитесь, что выдаются корректные значения для всех хостов.
### ![](https://github.com/Berezhok/ansible_one/blob/main/img/def_fact.png)
### При помощи ansible-vault зашифруйте факты в group_vars/deb и group_vars/el с паролем netology.
1. Зашифровали.
### Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь в работоспособности.
1. Сначала была ошибка. Но этой командой--ask-vault-password вроде исправилось и попросило пароль, выдало переменные в нормальном виде, хотя они и зашифрованы
### ![](https://github.com/Berezhok/ansible_one/blob/main/img/encrypt.png)
### Посмотрите при помощи ansible-doc список плагинов для подключения. Выберите подходящий для работы на control node.
1. Плагин local
### В prod.yml добавьте новую группу хостов с именем local, в ней разместите localhost с необходимым типом подключения.
### Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь, что факты some_fact для каждого из хостов определены из верных group_vars.
### ![](https://github.com/Berezhok/ansible_one/blob/main/img/local.png)
### Заполните README.md ответами на вопросы. Сделайте git push в ветку master. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым playbook и заполненным README.md.
### Предоставьте скриншоты результатов запуска команд.
1. Вроде основные команды есть в скринах 