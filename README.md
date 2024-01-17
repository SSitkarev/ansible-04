# Домашнее задание к занятию 4 «Работа с roles» - Сергей Ситкарёв

1. Создайте в старой версии playbook файл requirements.yml и заполните его содержимым:

---
  - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
    scm: git
    version: "1.13"
    name: clickhouse 

2. При помощи ansible-galaxy скачайте себе эту роль.

``` ansible-galaxy install -r requirements.yml -p roles ```

3. Создайте новый каталог с ролью при помощи ansible-galaxy role init vector-role.

``` ansible-galaxy role init roles/vector_role ```

``` ansible-galaxy role init roles/lighthouse_role ```

``` ansible-galaxy role init roles/clickhouse_role ```

4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между vars и default.

5. Перенести нужные шаблоны конфигов в templates.

6. Опишите в README.md обе роли и их параметры. Пример качественной документации ansible role по ссылке.

7. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.

8. Выложите все roles в репозитории. 

[group_vars](https://github.com/SSitkarev/ansible-04/tree/main/group_vars)

Проставьте теги, используя семантическую нумерацию. Добавьте roles в requirements.yml в playbook.

9. Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения roles с tasks.

10. Выложите playbook в репозиторий.

11. В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.