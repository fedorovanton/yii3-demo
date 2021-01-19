# Инструкция по установке

1. Выполнить сборку контейнеров докера: `docker-compose up -d --build`
2. Зайти в консоль докера: `docker-compose run web bash` и выполнить установку зависимостей `composer install`
3. Прописать в хостах компьютера (/etc/hosts): `127.0.0.1 yii3-demo.local`
4. Сайт доступен по URL:  http://yii3-demo.local
5. Выполнить миграции: `./vendor/bin/yii migrate/up`
6. Создать пользователя: `./vendor/bin/yii user/create demo demo`
7. Добавить фикстуры: `./vendor/bin/yii fixture/add 20`

## Доступы к БД

DB name: **yii3_demo_db**

DB user: **root**

DB password: **123456**

## Yii3

Документация (The Definitive Guide to Yii 3.0): https://github.com/yiisoft/docs/tree/master/guide/en

Приложение Yii3: https://github.com/yiisoft/app

#### Command for console

**Create new user**

`./vendor/bin/yii user/create <login> <password> [isAdmin = 0]`

**Assign RBAC role to user**

`./vendor/bin/yii user/assignRole <role> <userId>`

**Add random content**

`./vendor/bin/yii fixture/add [count = 10]`

**Migrations**

`./vendor/bin/yii migrate/create`
`./vendor/bin/yii migrate/generate`
`./vendor/bin/yii migrate/up`
`./vendor/bin/yii migrate/down` 
`./vendor/bin/yii migrate/list`

**DB Schema**

`./vendor/bin/yii cycle/schema`
`./vendor/bin/yii cycle/schema/php`
`./vendor/bin/yii cycle/schema/clear`
`./vendor/bin/yii cycle/schema/rebuild`