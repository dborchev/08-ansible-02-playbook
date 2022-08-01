# 08-ansible-02-playbook
см. https://github.com/dborchev/devops-netology/blob/main/08-ansible-02-playbook/README.md

### Playbook
Этот плейбук скачивает и устанавливает на целевые хосты группы `clickhouse` [clickhouse](https://clickhouse.com/) и [vector](https://vector.dev)
* в Clickhouse создется пустая база
* в Vector настраивается минимальный поток stdin->console в виде текста

Целевые хосты должны работать с пакетным менеджером yum

#### Параметры
* `clickhouse_version` определяет версию Clickhouse
* `vector_version` определяет версию Vector
* через список словарей `clickhouse_packages` и переменную `vector_arch` можно переопределить архитектуру процессора целевого хоста
