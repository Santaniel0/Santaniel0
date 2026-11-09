Пишу на Python и занимаюсь инфраструктурой: бэкенд, Telegram-боты, Linux-серверы, Terraform, Yandex Cloud. Больше всего меня интересует, что происходит с сервисом после деплоя: как он обновляется, переживает сбои и восстанавливается из бэкапа.

Ищу стажировку.

<img src="https://skillicons.dev/icons?i=python,fastapi,postgres,redis,terraform,linux,nginx,bash,githubactions" height="40" alt="Python, FastAPI, PostgreSQL, Redis, Terraform, Linux, nginx, Bash, GitHub Actions">

### Документация Yandex Cloud

Пишу практические руководства для [официальной документации](https://github.com/yandex-cloud/docs).

- **[Что делать при утечке статического ключа доступа](https://github.com/yandex-cloud/docs/pull/1118)** — принято.  
  Как найти сервисный аккаунт по `key_id`, проверить аудитные логи, перевыпустить ключ без простоя и удалить скомпрометированный.
- **[Защита резервных копий от удаления и перезаписи](https://github.com/yandex-cloud/docs/pull/1119)** — на ревью.  
  Блокировки версий объектов в Object Storage, чтобы бэкап нельзя было стереть ни по ошибке, ни при атаке.
- **[Проверка восстановления PostgreSQL и вложений Object Storage](https://github.com/yandex-cloud/docs/pull/1233)** — тема на согласовании.  
  Руководство к стенду, который описан ниже.

### Проекты

**[Бэкап под проверкой](https://github.com/Santaniel0/yandex-backup-under-test)**

Стенд, который проверяет, что резервная копия действительно восстанавливается. Поднимает PostgreSQL из бэкапа в отдельный кластер, сверяет данные и каждую версию файла в Object Storage по SHA-256, потом удаляет временные ресурсы. Если ответ API потерялся, повторно ничего не создаёт, а находит ресурс по меткам и убирает его. Прогнан в настоящем облаке, 32 теста.

`Python` `Terraform` `Cloud Functions` `Workflows` `pytest` `GitHub Actions`

**Telegram-бот для сервиса по подписке** · код закрыт

Коммерческий проект в продакшне. Бот и Telegram Mini App, оплата, реферальная и партнёрская программы, аналитика для админов. Инфраструктура тоже своя: nginx, автообновление по systemd-таймерам, миграции базы, закрытый SSH и файрвол.

`aiogram 3` `FastAPI` `PostgreSQL` `SQLAlchemy` `Alembic` `Redis` `nginx` `systemd`
