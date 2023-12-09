# zero

Это чистый шаблон проект на технологиях docker/nginx/php/mysql. Необходим для разработки нового проекта с нуля на docker.

Сделать полное описание каждого файла в структуре этого проекта на технологиях: docker/nginx/php/mysql

Стандартные репозитории и файлы для нового проекта на docker:

<img width="180" alt="index php" src="https://github.com/al-zv/zero/assets/63869857/77fd833a-1d9b-4e59-96e5-4f60e80f1e69">

zero - наименование репозитория проекта

zero/docker-compose.yml - главный файл docker


zero/nginx - репозиторий для настроек веб-сервера nginx

zero/nginx/core - репозиторий для настроек веб-сервера nginx

zero/nginx/core/nginx.conf - файл с настройками веб-сервера nginx


zero/nginx/www/app - репозиторий с кодом проекта

zero/nginx/www/app/index.php - индексный файл php для проверки работы docker


zero/php - репозиторий с настройками PHP для docker

zero/php/Dockerfile - файл с настройками PHP для docker

### <a name="21">1. Инструкция по запуску проекта</a> 

Скачать с GitHub

    git clone https://github.com/al-zv/zero.git folder

        folder - репозиторий, который будет создан в текущем репозитории

После скачивания проекта нужно проверить имя пользователя проекта командой:

    git config user.name

Если нужно локально (только для этого проекта) иное имя пользователя, то командой нужно сменить пользователя:

    git config user.name name

Также нужно проверить email пользователя проекта командой:

    git config user.email

Если нужно локально (только для этого проекта) иной email пользователя, то командой нужно сменить пользователя:

    git config user.email email

Также нужно изменить название удаленного репозитория на github командой:

    git remote set-url origin https://github.com/al-zv/oop.git

Далее в новый репозиторий нужно выложить код проекта командой:

    git push

Если для установки проекта/фреймворка нужен composer, то нужно запустить докер чтобы установился composer, а также php со всеми необходимыми расширениями, mysql и прочие нужные вещи для проекта. Запуск docker командой (первый раз запуск docker будет длительным):

    docker-compose up -d


DIRECTORY STRUCTURE - нужно так сделать для файлов описания содержимого репозитория

    common
        config/              contains shared configurations
        mail/                contains view files for e-mails
        models/              contains model classes used in both backend and frontend
        tests/               contains tests for common classes    
    console
        config/              contains console configurations
        controllers/         contains console controllers (commands)
        migrations/          contains database migrations
        models/              contains console-specific model classes
        runtime/             contains files generated during runtime
    backend
        assets/              contains application assets such as JavaScript and CSS
        config/              contains backend configurations
        controllers/         contains Web controller classes
        models/              contains backend-specific model classes
        runtime/             contains files generated during runtime
        tests/               contains tests for backend application    
        views/               contains view files for the Web application
        web/                 contains the entry script and Web resources
    frontend
        assets/              contains application assets such as JavaScript and CSS
        config/              contains frontend configurations
        controllers/         contains Web controller classes
        models/              contains frontend-specific model classes
        runtime/             contains files generated during runtime
        tests/               contains tests for frontend application
        views/               contains view files for the Web application
        web/                 contains the entry script and Web resources
        widgets/             contains frontend widgets
    vendor/                  contains dependent 3rd-party packages
    environments/            contains environment-based overrides
