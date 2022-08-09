# 08-ansible-02-playbook
см. https://github.com/dborchev/devops-netology/blob/main/08-ansible-02-playbook/README.md

### Playbook
Этот плейбук скачивает и устанавливает на целевые хосты группы `clickhouse` [clickhouse](https://clickhouse.com/),[vector](https://vector.dev), и [LightHouse](https://github.com/VKCOM/lighthouse)
* в Clickhouse создется пустая база
* в Vector настраивается минимальный поток stdin->console в виде текста
* LightHouse всегда последней версии из репозитория, обслуживается nginx последней версии доступной в EPEL

Целевые хосты должны работать с пакетным менеджером yum

#### Параметры
* `clickhouse_version` определяет версию Clickhouse
* `vector_version` определяет версию Vector
* через список словарей `clickhouse_packages` и переменную `vector_arch` можно переопределить архитектуру процессора целевого хоста
* используя `document_root` можно указать альтернативный путь распаковки LightHouse