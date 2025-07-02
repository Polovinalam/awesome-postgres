# Awesome Postgres [![awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

[<img src="https://wiki.postgresql.org/images/a/a4/PostgreSQL_logo.3colors.svg" align="right" width="100">](https://www.postgresql.org/)

> Кураторский список потрясающего ПО, библиотек, инструментов и ресурсов для [PostgreSQL](https://www.postgresql.org/), вдохновленный [awesome-mysql](http://shlomi-noach.github.io/awesome-mysql/)

[PostgreSQL](https://en.wikipedia.org/wiki/PostgreSQL), часто называемый просто Postgres, — это [объектно-реляционная СУБД](https://en.wikipedia.org/wiki/Object-relational_database) (ORDBMS). PostgreSQL соответствует принципам [ACID](https://en.wikipedia.org/wiki/ACID) и поддерживает [транзакции](https://en.wikipedia.org/wiki/Transaction_processing). (подробнее: [Wikipedia:PostgreSQL](https://en.wikipedia.org/wiki/PostgreSQL), [PostgreSQL.org](https://www.postgresql.org))

:elephant: Приветствуются contributions. Добавляйте ссылки через [pull requests](https://github.com/dhamaniasad/awesome-postgres/pulls) или создавайте [issue](https://github.com/dhamaniasad/awesome-postgres/issues) для обсуждения. Пожалуйста, ознакомьтесь с [правилами внесения вклада](CONTRIBUTING.md).

## Содержание

- [Awesome Postgres](#awesome-postgres-)
  - [Высокая доступность](#высокая-доступность)
  - [Резервное копирование](#резервное-копирование)
  - [Графические интерфейсы](#графические-интерфейсы)
  - [Дистрибутивы](#дистрибутивы)
  - [CLI](#cli)
  - [Сервер](#сервер)
  - [Мониторинг](#мониторинг)
  - [Расширения](#расширения)
  - [Очереди задач](#очереди-задач)
  - [Оптимизация](#оптимизация)
  - [Утилиты](#утилиты)
  - [Языковые привязки](#языковые-привязки)
  - [PaaS (PostgreSQL как сервис)](#paas-postgresql-как-сервис)
  - [Docker-образы](#docker-образы)
  - [Kubernetes](#kubernetes)
- [Ресурсы](#ресурсы)
  - [Обучающие материалы](#обучающие-материалы)
  - [Блоги](#блоги)
  - [Статьи](#статьи)
  - [Книги](#книги)
  - [Документация](#документация)
  - [Рассылки](#рассылки)
  - [Подкасты](#подкасты)
  - [Видео](#видео)
  - [Сообщество](#сообщество)
  - [Дорожные карты](#дорожные-карты)
  - [Внешние списки](#внешние-списки)

### Высокая доступность
* [autobase](https://github.com/vitabaks/autobase) - Autobase для PostgreSQL® — это open-source DBaaS, автоматизирующий развертывание и управление высокодоступными кластерами PostgreSQL.
* [BDR](https://github.com/2ndQuadrant/bdr) - BiDirectional Replication — система multimaster-репликации для PostgreSQL.
* [Patroni](https://github.com/zalando/patroni) - Шаблон для обеспечения высокой доступности PostgreSQL с ZooKeeper или etcd.
* [Stolon](https://github.com/sorintlab/stolon) - Высокая доступность PostgreSQL на основе Consul или etcd с интеграцией Kubernetes.
* [pglookout](https://github.com/aiven/pglookout) - Демон мониторинга репликации и переключения при сбоях.
* [repmgr](https://github.com/2ndQuadrant/repmgr) - Набор open-source инструментов для управления репликацией и переключением в кластере серверов PostgreSQL.
* [Slony-I](https://slony.info/) - Система репликации "master-to-multiple slaves" с каскадированием и переключением при сбоях.
* [PAF](https://github.com/ClusterLabs/PAF) - PostgreSQL Automatic Failover: высокая доступность для Postgres на основе Pacemaker и Corosync.
* [SkyTools](https://github.com/pgq/skytools-legacy) - Инструменты репликации, включая PgQ (систему очередей) и Londiste (систему репликации, более простую в управлении, чем Slony).
* [pg_auto_failover](https://github.com/citusdata/pg_auto_failover) - Расширение и сервис PostgreSQL для автоматического переключения при сбоях и обеспечения высокой доступности.
* [pgrwl](https://github.com/hashmap-kz/pgrwl) - Потоковая передача write-ahead логов (WAL) с сервера PostgreSQL в реальном времени. Контейнерная альтернатива pg_receivewal.

### Резервное копирование
* [Barman](https://www.pgbarman.org/index.html) - Менеджер резервного копирования и восстановления PostgreSQL от 2ndQuadrant.
* [OmniPITR](https://github.com/omniti-labs/omnipitr) - Продвинутые инструменты управления WAL-файлами для PostgreSQL.
* [pg_probackup](https://github.com/postgrespro/pg_probackup) – Форк pg_arman, улучшенный PostgresPro, поддерживает инкрементное резервное копирование, резервное копирование с реплики, многопоточное резервное копирование и восстановление, а также анонимное резервное копирование без команды archive.
* [pgBackRest](https://pgbackrest.org/) - Надежное резервное копирование и восстановление PostgreSQL.
* [pgbackweb](https://github.com/eduardolat/pgbackweb) - Полноценный инструмент для резервного копирования и обслуживания Postgres на основе Docker с веб-интерфейсом.
* [pg_back](https://github.com/orgrim/pg_back/) - Простой скрипт для резервного копирования.
* [pghoard](https://github.com/aiven/pghoard) - Инструмент резервного копирования и восстановления для облачных object storage (AWS S3, Azure, Google Cloud, OpenStack Swift).
* [wal-e](https://github.com/wal-e/wal-e) (устаревший) - Простое непрерывное архивирование для PostgreSQL в S3, Azure или Swift от Heroku.
* [wal-g](https://github.com/wal-g/wal-g) - Преемник WAL-E, переписанный на Go. Поддерживает облачные хранилища AWS (S3), Google Cloud (GCS), Azure, OpenStack Swift, MinIO и файловые системы. Поддерживает инкрементное резервное копирование на уровне блоков, выгрузку задач резервного копирования на standby-сервер, предоставляет опции параллелизации и регулирования. Помимо Postgres, WAL-G можно использовать для MySQL и MongoDB.
* [pitrery](https://dalibo.github.io/pitrery/) - Набор Bash-скриптов для управления резервными копиями Point In Time Recovery (PITR) в PostgreSQL.
* [pgbackup-sidecar](https://github.com/Musab520/pgbackup-sidecar) - Легковесный Docker sidecar-контейнер для автоматизации регулярного резервного копирования PostgreSQL с использованием pg_dump, cron и bash-скриптов с отправкой результатов в webhook.
* [pg-backups-to-s3](https://github.com/Saicheg/pg-backups-to-s3) - Решение на основе Docker поверх pg_dump с поддержкой конфигурации на основе окружения для запланированного резервного копирования PostgreSQL с опциональным сжатием, GPG-шифрованием, webhooks и автоматической загрузкой в Amazon S3.

### Графические интерфейсы
* [Adminer](https://www.adminer.org/) - Полнофункциональный инструмент управления базами данных на PHP.
* [Beekeeper Studio](https://www.beekeeperstudio.io) - Бесплатный и открытый SQL-клиент с современным интерфейсом и отличной поддержкой Postgres. Кроссплатформенный.
* [Chartbrew](https://chartbrew.com) - Создание интерактивных дашбордов, графиков и отчетов из данных PostgreSQL. Включает инструмент запросов, работающий с SQL.
* [Count](https://count.co/) - Веб-платформа аналитики с интерфейсом блокнота, подключающаяся к PostgreSQL (Проприетарное ПО).
* [DataGrip](https://www.jetbrains.com/datagrip/) - IDE с продвинутыми инструментами и отличным кроссплатформенным опытом (Проприетарное ПО).
* [Datazenit](https://datazenit.com/) - Веб-интерфейс для PostgreSQL (Проприетарное ПО).
* [DataRow](https://www.datarow.com/) - Кроссплатформенный SQL-клиент для Amazon Redshift: простой, удобный, расширяемый.
* [DBConvert Streams](https://streams.dbconvert.com/) - Облачная платформа для миграции данных в реальном времени и CDC-репликации между PostgreSQL и MySQL в различных облачных средах (Проприетарное ПО).
* [DBeaver](https://dbeaver.io/) - Универсальный менеджер баз данных с отличной поддержкой PostgreSQL.
* [DbVisualizer](http://www.dbvis.com) - Кроссплатформенный клиент для разработчиков, DBA и аналитиков (Проприетарное ПО).
* [Holistics](https://www.holistics.io/) - Онлайн-инструмент управления базами данных и SQL-отчетов с мощной поддержкой PostgreSQL (Проприетарное ПО).
* [JackDB](https://www.jackdb.com/) - Веб-интерфейс для SQL-запросов (Проприетарное ПО).
* [Luna Modeler](http://www.datensen.com) - Кроссплатформенный инструмент моделирования данных (Проприетарное ПО).
* [Mathesar](https://mathesar.org/) - Веб-приложение, предоставляющее интуитивно понятный пользовательский интерфейс для работы с базами данных.
* [Metabase](https://www.metabase.com/) - Простые дашборды, графики и инструмент запросов для PostgreSQL.
* [Numeracy](https://numeracy.co/) - Быстрый SQL-редактор с графиками и дашбордами для PostgreSQL (Проприетарное ПО).
* [pgAdmin](https://www.pgadmin.org/) - Графический интерфейс для администрирования PostgreSQL.
* [pgMagic🪄](https://pgmagic.app/?ref=awesomepostgres) - Общайтесь с Postgres на естественном языке (Проприетарное ПО).
* [pgModeler](https://pgmodeler.io/) - pgModeler — это open-source инструмент для моделирования баз данных PostgreSQL.
* [pgweb](https://github.com/sosedoff/pgweb) - Веб-браузер баз данных PostgreSQL, написанный на Go.
* [phpPgAdmin](https://github.com/phppgadmin/phppgadmin) - Веб-интерфейс для администрирования PostgreSQL.
* [Postbird](https://github.com/Paxa/postbird) - Клиент PostgreSQL для macOS.
* [PostgresCompare](https://www.postgrescompare.com) - Кроссплатформенный инструмент сравнения и развертывания баз данных (Проприетарное ПО).
* [Postico](https://eggerapps.at/postico/) - Современный клиент PostgreSQL для macOS (Проприетарное ПО).
* [PSequel](http://www.psequel.com/) - Простой интерфейс для быстрого выполнения распространенных задач PostgreSQL (Проприетарное ПО).
* [Redash](https://github.com/getredash/redash) - Подключайтесь к любым источникам данных, легко визуализируйте и делитесь данными.
* [SQL Tabs](http://www.sqltabs.com/) - Кроссплатформенный десктопный клиент PostgreSQL на JS.
* [SQLPro for Postgres](http://macpostgresclient.com/) - Простой и мощный менеджер PostgreSQL для macOS (Проприетарное ПО).
* [temBoard](https://github.com/dalibo/temboard) - Веб-интерфейс для мониторинга PostgreSQL.
* [Teable](https://github.com/teableio/teable) - Супербыстрая, реального времени, профессиональная, дружелюбная к разработчикам no-code база данных.
* [TablePlus](https://tableplus.com/) - Нативное приложение для редактирования структуры и данных базы данных с высоким уровнем безопасности (Проприетарное ПО).
* [Valentina Studio](https://www.valentina-db.com/en/valentina-studio-overview) - Кроссплатформенный инструмент администрирования баз данных (Бесплатно/Проприетарное).
* [DbGate](https://dbgate.org) - Самый умный клиент для (no)SQL баз данных.
* [WebDB](https://webdb.app) – Эффективная IDE для баз данных.

### Дистрибутивы
* [Postgres.app](https://postgresapp.com/) - Самый простой способ начать работу с PostgreSQL на macOS.
* [Pigsty](https://github.com/Vonng/pigsty) - Готовый к использованию open-source дистрибутив PostgreSQL с расширенной наблюдаемостью и инструментарием Database-as-Code для разработчиков.

### CLI
* [atlas](https://github.com/ariga/atlas) - Инструмент для управления и миграции схем баз данных с использованием принципов DevOps.
* [pgcli](https://github.com/dbcli/pgcli) - CLI для Postgres с автодополнением и подсветкой синтаксиса.
* [pg-schema-diff](https://github.com/stripe/pg-schema-diff) - CLI (и библиотека Golang) для сравнения схем Postgres и генерации SQL-миграций с минимальной блокировкой.
* [pgsh](https://github.com/sastraxi/pgsh) - Ветвление базы данных PostgreSQL как в Git.
* [psql](https://www.postgresql.org/docs/current/static/app-psql.html) - Встроенный CLI-клиент PostgreSQL.
* [psql2csv](https://github.com/fphilipe/psql2csv) - Выполнение запросов в psql с выводом результатов в CSV.
* [schemaspy](https://github.com/schemaspy/schemaspy) - SchemaSpy — это инструмент на Java JDBC для генерации HTML-документации вашей базы данных, включая диаграммы "сущность-связь".
* [pdot](https://gitlab.com/dmfay/pdot) - Визуализация и исследование структур базы данных в вашей оболочке: от общего представления графа внешних ключей до каскадов триггеров, наследования ролей и прав доступа.

### Сервер
* [AgensGraph](https://bitnine.net/) - Мощная графовая база данных на основе PostgreSQL.
* [Apache Cloudberry](https://github.com/apache/cloudberry) - MPP-форк PostgreSQL. Open-source альтернатива Greenplum Database.
* [FerretDB](https://www.ferretdb.io) - По-настоящему открытая альтернатива MongoDB поверх PostgreSQL.
* [Postgres-XL](https://www.postgres-xl.org/) - Масштабируемый кластер баз данных на основе PostgreSQL.
* [YugabyteDB](https://yugabyte.com/) - Open-source распределенная SQL-СУБД, использующая форк PostgreSQL поверх распределенного хранилища и транзакций.

### Безопасность
* [Acra](https://github.com/cossacklabs/acra) - Набор инструментов безопасности для SQL-баз данных: прокси для защиты данных с прозрачным шифрованием "на лету", SQL-брандмауэр (защита от инъекций), система обнаружения вторжений.

### Мониторинг
* [check_pgactivity](https://github.com/OPMDG/check_pgactivity) - Инструмент для мониторинга кластеров PostgreSQL из Nagios. Предоставляет множество опций для измерения и отслеживания полезных метрик производительности.
* [Check_postgres](https://github.com/bucardo/check_postgres) - Плагин Nagios check_postgres для проверки состояния баз данных PostgreSQL.
* [coroot](https://github.com/coroot/coroot) - Coroot — это open-source инструмент APM и Observability, альтернатива DataDog и NewRelic. Использует eBPF для быстрого анализа производительности системы.
* [Datadog](https://www.datadoghq.com/product/database-monitoring/) - SaaS-мониторинг, который собирает и визуализирует метрики, запросы и планы выполнения, а также отправляет оповещения при возникновении проблем (Проприетарное ПО).
* [Instrumental](https://github.com/Instrumental/instrumentald) - Мониторинг производительности в реальном времени, включая [готовые графики](https://instrumentalapp.com/docs/instrumentald/postgresql#suggested-graphs) для быстрой настройки (Проприетарное ПО).
* [libzbxpgsql](https://github.com/cavaliercoder/libzbxpgsql) - Комплексный модуль мониторинга PostgreSQL для Zabbix.
* [PMM](https://github.com/percona/pmm) - Percona Monitoring and Management (PMM) — это бесплатная open-source платформа для мониторинга и управления PostgreSQL, MySQL и MongoDB.
* [Pome](https://github.com/rach/pome) - Pome означает PostgreSQL Metrics. Pome — это дашборд метрик PostgreSQL для отслеживания состояния вашей базы данных.
* [pgmetrics](https://pgmetrics.io/) - pgmetrics — это open-source инструмент без зависимостей, собирающий информацию и статистику с работающего сервера PostgreSQL и отображающий ее в удобочитаемом текстовом формате или экспортирующий в JSON и CSV для скриптов.
* [pg_view](https://github.com/zalando/pg_view) - Инструмент командной строки с открытым исходным кодом, показывающий глобальную статистику системы, информацию по партициям, статистику памяти и другую информацию.
* [pgwatch2](https://github.com/cybertec-postgresql/pgwatch2) - Гибкий и простой в настройке монитор метрик PostgreSQL с фокусом на дашборды Grafana.
* [pgbench](https://www.postgresql.org/docs/devel/static/pgbench.html) - Запуск тестов производительности PostgreSQL.
* [opm.io](http://opm.io) - Open PostgreSQL Monitoring — это бесплатный набор инструментов для управления серверами PostgreSQL. Может собирать статистику, отображать дашборды и отправлять предупреждения при возникновении проблем.
* [okmeter.io](https://okmeter.io/pg) - Коммерческий SaaS-мониторинг на основе агентов с очень детальным плагином PostgreSQL. Автоматически собирает сотни метрик, отображает дашборды по всем аспектам и отправляет оповещения при проблемах (Проприетарное ПО).
* [dexter](https://github.com/ankane/dexter) - Автоматический индексатор для Postgres. Обнаруживает медленные запросы и создает индексы, если настроено.
* [pg_exporter](https://github.com/Vonng/pg_exporter) - Полностью настраиваемый экспортер Prometheus для PostgreSQL и Pgbouncer с детальным контролем выполнения.
* [postgres_exporter](https://github.com/wrouesnel/postgres_exporter) - Экспортер метрик сервера PostgreSQL для Prometheus.

### Расширения
* [AGE](https://github.com/apache/age) - Добавляет полнофункциональную поддержку графовых баз данных, включая запросы Cypher.
* [OrioleDB](https://www.orioledb.com/) - Облачное хранилище для PostgreSQL. OrioleDB — это расширение PostgreSQL, сочетающее преимущества дисковых и in-memory движков.
* [Citus](https://github.com/citusdata/citus) - Масштабируемый кластер PostgreSQL для рабочих нагрузок реального времени.
* [cstore_fdw](https://github.com/citusdata/cstore_fdw) - Колоночное хранилище для аналитики в PostgreSQL.
* [cyanaudit](https://pgxn.org/dist/cyanaudit/) - Cyan Audit предоставляет журналирование всех DML-операций в базе данных с детализацией по столбцам.
* [pg_analytics](https://github.com/paradedb/pg_analytics) - pg_analytics — это расширение, ускоряющее обработку аналитических запросов в Postgres до уровня, сравнимого с выделенными OLAP-базами данных.
* [pg_lakehouse](https://github.com/paradedb/paradedb/tree/dev/pg_lakehouse) - pg_lakehouse — это расширение, превращающее Postgres в аналитический движок для object storage (AWS S3/GCS) и табличных форматов (Delta Lake/Iceberg).
* [pg_search](https://github.com/paradedb/paradedb/tree/dev/pg_search) - pg_search — это расширение PostgreSQL, обеспечивающее полнотекстовый поиск по SQL-таблицам с использованием алгоритма BM25, современной функции ранжирования для полнотекстового поиска.
* [pg_cron](https://github.com/citusdata/pg_cron) - Запуск периодических задач в PostgreSQL.
* [pglogical](https://github.com/2ndQuadrant/pglogical) - Расширение, предоставляющее логическую потоковую репликацию.
* [pgcat](https://github.com/kingluo/pgcat) - Улучшенная логическая репликация PostgreSQL.
* [pg_barcode](https://github.com/btouchard/pg_barcode/) - Генератор SVG QR-кодов и Datamatrix для PostgreSQL.
* [pg_partman](https://github.com/pgpartman/pg_partman) - Расширение для управления партициями в PostgreSQL.
* [pg_paxos](https://github.com/citusdata/pg_paxos/) - Базовая реализация Paxos и репликации таблиц на основе Paxos для кластера узлов PostgreSQL.
* [pg_shard](https://github.com/citusdata/pg_shard) - Расширение для масштабирования операций чтения и записи в реальном времени.
* [pg_stat_monitor](https://github.com/percona/pg_stat_monitor) - Инструмент мониторинга производительности запросов PostgreSQL.
* [pg_squeeze](https://github.com/cybertec-postgresql/pg_squeeze) - Расширение для автоматической очистки "раздувания" с минимальной блокировкой.
* [PGStrom](https://wiki.postgresql.org/wiki/PGStrom) - Расширение для выгрузки CPU-интенсивных задач на GPU.
* [pgxn](https://pgxn.org/) - Сеть расширений PostgreSQL — центральная точка распространения многих open-source расширений PostgreSQL.
* [PipelineDB](https://www.confluent.io/blog/pipelinedb-team-joins-confluent/) - Расширение PostgreSQL, непрерывно выполняющее SQL-запросы над потоками данных, инкрементально сохраняя результаты в таблицах.
* [plpgsql_check](https://github.com/okbob/plpgsql_check) - Расширение для проверки исходного кода plpgsql.
* [PostGIS](http://postgis.net/) - Пространственные и географические объекты для PostgreSQL.
* [PG_Themis](https://github.com/cossacklabs/pg_themis) - Привязка Postgres как расширение для криптографической библиотеки Themis, предоставляющей различные сервисы безопасности на стороне PgSQL.
* [zomboDB](https://github.com/zombodb/zombodb) - Расширение, обеспечивающее эффективный полнотекстовый поиск через индексы, поддерживаемые Elasticsearch.
* [pgMemento](https://github.com/pgMemento/pgMemento) - Обеспечивает аудит данных в базе PostgreSQL с использованием триггеров и серверных функций на PL/pgSQL.
* [TimescaleDB](https://www.timescale.com/) - Open-source time-series база данных, полностью совместимая с Postgres, распространяемая как расширение.
* [pgTAP](https://pgtap.org/) - Фреймворк для тестирования баз данных Postgres.
* [HypoPG](https://github.com/HypoPG/hypopg) - HypoPG предоставляет функциональность гипотетических/виртуальных индексов.
* [pgRouting](https://github.com/pgRouting/pgrouting) - pgRouting расширяет геопространственную базу данных PostGIS/PostgreSQL, предоставляя функциональность геопространственной маршрутизации и другого сетевого анализа.
* [PGroonga](https://pgroonga.github.io/) - PGroonga предоставляет новый метод доступа к индексам с использованием Groonga, позволяющий осуществлять сверхбыстрый полнотекстовый поиск на всех языках.
* [PGAudit](https://www.pgaudit.org/) - Расширение PostgreSQL Audit (или pgaudit) предоставляет детальное журналирование аудита сеансов и/или объектов через стандартный механизм логирования PostgreSQL.
* [PostgresML](https://postgresml.org/) - Машинное обучение и ИИ внутри вашей базы данных, включая векторы, LLM и классическое ML. Обучайте, предсказывайте и управляйте всем жизненным циклом моделей машинного обучения, используя только SQL.
* [ParadeDB](https://github.com/paradedb/paradedb) - Postgres для поиска и аналитики.

### Очереди задач
* [BeanQueue](https://github.com/LaunchPlatform/bq) - Фреймворк для очередей задач на Python, основанный на SKIP LOCKED, LISTEN и NOTIFY.
* [pgmq](https://github.com/pgmq/pgmq) - Легковесная очередь сообщений. Как AWS SQS и RSMQ, но на Postgres.
* [river](https://github.com/riverqueue/river) - Высокопроизводительная система обработки задач для Go и Postgres.

### Оптимизация
* [EverSQL](https://www.eversql.com/) - Инструмент автоматической оптимизации запросов, мониторинга и анализа, рекомендаций по индексации (Проприетарное ПО).
* [PEV2](https://github.com/dalibo/pev2) - Визуализатор EXPLAIN для PostgreSQL онлайн.
* [pg_flame](https://github.com/mgartner/pg_flame) - Генератор flamegraph для планов запросов.
* [PgHero](https://github.com/ankane/pghero) - Упрощенный анализ PostgreSQL.
* [pgMustard](https://www.pgmustard.com/) - Современный интерфейс для `EXPLAIN`, также предоставляющий рекомендации по производительности (Проприетарное ПО).
* [pgtune](https://github.com/gregs1104/pgtune/) - Мастер настройки конфигурации PostgreSQL.
* [pgtune](https://github.com/le0pard/pgtune) - Онлайн-версия мастера настройки конфигурации PostgreSQL.
* [pgconfig.org](https://github.com/sebastianwebber/pgconfig) - Онлайн-инструмент настройки PostgreSQL (также основанный на pgtune).
* [PoWA](https://powa.readthedocs.io/en/latest/) - Анализатор рабочей нагрузки PostgreSQL собирает статистику производительности и предоставляет графики в реальном времени для мониторинга и настройки серверов PostgreSQL.
* [pg_web_stats](https://github.com/kirs/pg_web_stats) - Веб-интерфейс для просмотра pg_stat_statements.
* [TimescaleDB Tune](https://github.com/timescale/timescaledb-tune) - Программа для настройки базы данных TimescaleDB для максимальной производительности на основе ресурсов хоста, таких как память и количество CPU.
* [Metis](https://www.metisdata.io/product/troubleshooting) - Metis предоставляет наблюдаемость и настройку производительности для SQL-баз данных, включая PostgreSQL (Проприетарное ПО).
* [aqo](https://github.com/postgrespro/aqo) - Адаптивная оптимизация запросов для PostgreSQL.
* [pgassistant](https://github.com/nexsol-technologies/pgassistant) - Дашборд оптимизации баз данных PostgreSQL с интеграцией LLM и pgTune.

### Утилиты
* [apgdiff](https://www.apgdiff.com/) - Сравнивает два дампа базы данных и создает выходные данные с DDL-операторами для обновления старой схемы базы данных до новой.
* [bemi](https://github.com/BemiHQ/bemi) - Автоматическое отслеживание изменений данных для PostgreSQL.
* [ERAlchemy](https://github.com/Alexis-benoist/eralchemy) - ERAlchemy генерирует диаграмму "сущность-связь" из баз данных.
* [flyway](https://flywaydb.org/) - Инструмент миграции схем для Postgres и других СУБД.
* [GatewayD](https://github.com/gatewayd-io/gatewayd) - Облачный шлюз для баз данных и фреймворк для создания data-driven приложений. Как API-шлюзы, но для баз данных.
* [Hasura GraphQL Engine](https://github.com/hasura/graphql-engine) - Молниеносные GraphQL API в реальном времени на Postgres с детальным контролем доступа и webhooks на события базы данных.
* [ldap2pg](https://github.com/dalibo/ldap2pg) - Синхронизация ролей и прав из YML и LDAP.
* [migra](https://github.com/djrobstep/migra) - Как diff, но для схем Postgres.
* [mysql-postgresql-converter](https://github.com/lanyrd/mysql-postgresql-converter) - Скрипт преобразования MySQL в PostgreSQL от Lanyrd.
* [NServiceBus.Transport.PostgreSql](https://github.com/Particular/NServiceBus.SqlServer) - Библиотека NServiceBus.Transport.PostgreSql позволяет .NET-разработчикам [использовать базу данных PostgreSQL как брокер сообщений](https://docs.particular.net/transports/postgresql) (Проприетарное ПО).
* [ora2pg](http://ora2pg.darold.net) - Perl-модуль для экспорта схемы базы данных Oracle в схему, совместимую с PostgreSQL.
* [pg_activity](https://github.com/dalibo/pg_activity) - Приложение типа top для мониторинга активности сервера PostgreSQL.
* [pg-formatter](https://github.com/gajus/pg-formatter) - Форматировщик SQL-синтаксиса PostgreSQL (Node.js).
* [pganalyze](https://pganalyze.com) - Мониторинг производительности PostgreSQL (Проприетарное ПО).
* [pgbadger](https://github.com/darold/pgbadger) - Быстрый анализатор логов PostgreSQL.
* [PgBouncer](http://www.pgbouncer.org/) - Легковесный пулер соединений для PostgreSQL.
* [pgCenter](https://github.com/lesovsky/pgcenter) - Предоставляет удобный интерфейс для различных статистик, задач управления, перезагрузки сервисов, просмотра логов и отмены/завершения процессов базы данных.
* [pg_chameleon](https://github.com/the4thdoctor/pg_chameleon) - Репликация в реальном времени из MySQL в PostgreSQL с возможностью переопределения типов и миграции.
* [pgclimb](https://github.com/lukasmartinelli/pgclimb) - Экспорт данных из PostgreSQL в различные форматы.
* [pg_docs_bot](https://github.com/mchristofides/pg_docs_bot/) - Расширение браузера для перенаправления ссылок на документацию PostgreSQL на текущую версию.
* [pgfutter](https://github.com/lukasmartinelli/pgfutter) - Простой способ импорта CSV и JSON в PostgreSQL.
* [PGInsight](http://pginsight.io/) - Инструмент командной строки для легкого анализа вашей базы данных PostgreSQL.
* [pg_insights](https://github.com/lob/pg_insights) - Удобный SQL для мониторинга состояния базы данных Postgres.
* [pgloader](https://github.com/dimitri/pgloader) - Загружает данные в PostgreSQL с использованием протокола COPY, используя отдельные потоки для чтения и записи данных.
* [pgMonitor](https://github.com/CrunchyData/pgmonitor) - Сбор и визуализация метрик Postgres, который можно развернуть на bare metal, виртуальных машинах или Kubernetes.
* [pgpool-II](https://www.pgpool.net/mediawiki/index.php/Main_Page) - Промежуточное ПО, предоставляющее пулинг соединений, репликацию, балансировку нагрузки и ограничение превышения количества соединений.
* [pgspot](https://github.com/timescale/pgspot) - Обнаружение уязвимостей в скриптах расширений PostgreSQL.
* [pg-spot-operator](https://github.com/pg-spot-ops/pg-spot-operator) - Демон для запуска PostgreSQL на недорогих виртуальных машинах AWS Spot.
* [pgsync](https://github.com/ankane/pgsync) - Инструмент для синхронизации данных PostgreSQL с вашим локальным компьютером.
* [PGXN client](https://github.com/pgxn/pgxnclient) - Инструмент командной строки для взаимодействия с сетью расширений PostgreSQL.
* [postgresql-metrics](https://github.com/spotify/postgresql-metrics) - Инструмент, который извлекает и предоставляет метрики для вашей базы данных PostgreSQL.
* [PostgREST](https://github.com/PostgREST/postgrest) - Предоставляет полностью RESTful API из любой существующей базы данных PostgreSQL.
* [pREST](https://github.com/prest/prest) - Предоставляет RESTful API из любой базы данных PostgreSQL (на Golang).
* [PostGraphile](https://github.com/graphile/postgraphile) - Мгновенный GraphQL API или схема GraphQL для вашей базы данных PostgreSQL.
* [yoke](https://github.com/nanopack/yoke) - Кластер PostgreSQL с высокой доступностью, автоматической переключаемостью и автоматическим восстановлением кластера.
* [pglistend](https://github.com/kabirbaidhya/pglistend) - Легковесный демон PostgresSQL `LISTEN`/`NOTIFY`, построенный на основе `node-postgres`.
* [ZSON](https://github.com/postgrespro/zson) - Расширение PostgreSQL для прозрачного сжатия JSONB.
* [pg_bulkload](http://ossc-db.github.io/pg_bulkload/index.html) - Утилита для высокоскоростной загрузки данных в PostgreSQL.
* [pg_migrate](https://github.com/jwdeitch/pg_migrate) - Управление кодовыми базами PostgreSQL и упрощение работы с системами контроля версий.
* [pg_timetable](https://github.com/cybertec-postgresql/pg_timetable) - Расширенный планировщик задач для PostgreSQL.
* [sqitch](https://github.com/sqitchers/sqitch) - Инструмент для управления развертыванием версионированных схем.
* [pgmigrate](https://github.com/yandex/pgmigrate) - Инструмент командной строки для эволюции миграций схем, разработанный компанией Yandex.
* [pgcmp](https://github.com/cbbrowne/pgcmp) - Инструмент для сравнения схем баз данных с возможностью принятия некоторых постоянных различий.
* [pg-differ](https://github.com/multum/pg-differ) - Инструмент для легкой инициализации / обновления структуры таблиц PostgreSQL, альтернатива миграции (Node.js).
* [sqlcheck](https://github.com/jarulraj/sqlcheck) - Автоматически обнаруживает распространенные анти-паттерны SQL, которые часто замедляют запросы. Их исправление поможет ускорить запросы.
* [postgres-checkup](https://gitlab.com/postgres-ai/postgres-checkup) - инструмент диагностики нового поколения, который позволяет пользователям собирать глубокий анализ состояния базы данных Postgres.
* [Pyrseas](https://github.com/perseas/Pyrseas) - Версионирование схемы базы данных Postgres.
* [ScaffoldHub.io](https://scaffoldhub.io) - Генерация полнофункциональных приложений PostgreSQL с Angular, Vue или React (Коммерческое ПО).
* [planter](https://github.com/achiku/planter) - Генерация текстового описания ER-диаграммы PlantUML из таблиц PostgreSQL.
* [pgroll](https://github.com/xataio/pgroll) - Миграции схемы Postgres с нулевым временем простоя и возможностью отката.
* [RegreSQL](https://github.com/dimitri/regresql) - Инструмент для создания, поддержки и выполнения набора регрессионных тестов для SQL-запросов.

### Привязки языков
* Common Lisp: [Postmodern](https://github.com/marijnh/Postmodern)
* Clojure: [clj-postgresql](https://github.com/remodoy/clj-postgresql)
* Elixir: [postgrex](https://github.com/elixir-ecto/postgrex)
* Go: [pq](https://github.com/lib/pq), [pgx](https://github.com/jackc/pgx), [go-pg](https://github.com/go-pg/pg)
* Haskell: [postgresql-simple](http://hackage.haskell.org/package/postgresql-simple)
* Java: [PostgreSQL JDBC Driver](https://jdbc.postgresql.org/), [Vert.x PostgreSQL Client](https://vertx.io/docs/vertx-pg-client/java/)
* Lua: [luapgsql](https://github.com/arcapos/luapgsql)
* .Net/.Net Core: [Npgsql](https://github.com/npgsql/npgsql)
* Node: [node-postgres](https://github.com/brianc/node-postgres), [pg-promise](https://github.com/vitaly-t/pg-promise), [pogi](https://github.com/holdfenytolvaj/pogi), [slonik](https://github.com/gajus/slonik), [postgres](https://github.com/porsager/postgres)
* Perl: [DBD-Pg](https://metacpan.org/pod/distribution/DBD-Pg/Pg.pm)
* PHP: [Pomm](http://www.pomm-project.org), [pecl/pq](https://github.com/m6w6/ext-pq)
* Python: [psycopg2](https://pypi.org/project/psycopg2/), [asyncpg](https://pypi.org/project/asyncpg/), [pg8000](https://pypi.org/project/pg8000/)
* R: [RPostgres](https://github.com/r-dbi/RPostgres), [RPostgreSQL](https://github.com/tomoakin/RPostgreSQL)
* Ruby: [pg](https://github.com/ged/ruby-pg)
* Rust: [rust-postgresql](https://github.com/sfackler/rust-postgres), [pgx](https://github.com/tcdi/pgx), [wtx](https://github.com/c410-f3r/wtx)
* TypeScript: [zapatos](https://github.com/jawj/zapatos)
* Zig: [pg.zig](https://github.com/karlseguin/pg.zig)

### PaaS *(PostgreSQL как сервис)*

* [Aiven PostgreSQL](https://aiven.io/postgresql) - PostgreSQL как сервис в AWS, Azure, DigitalOcean, Google Cloud и UpCloud; тарифы варьируются от $19/месяц за одноузловые инстансы до крупных высокодоступных настроек, бесплатный пробный период на две недели.
* [Amazon RDS for PostgreSQL](https://aws.amazon.com/rds/postgresql/) - Amazon Relational Database Service (RDS) для PostgreSQL.
* [Azure Database for PostgreSQL](https://azure.microsoft.com/en-us/services/postgresql/) - Azure Database for PostgreSQL предоставляет полностью управляемую, готовую к использованию в корпоративной среде базу данных PostgreSQL как сервис. Она обеспечивает встроенную высокую доступность, эластичное масштабирование и нативную интеграцию с экосистемой Azure.
* [Crunchy Bridge](https://www.crunchydata.com/products/crunchy-bridge/) - Полностью управляемый Postgres от экспертов Postgres. Доступен во всех основных облачных провайдерах: Amazon AWS, Google GCP, Microsoft Azure. Нет привязки с полной поддержкой суперпользователя.
* [Database Labs](https://www.databaselabs.io) - Получите готовый к использованию облачный сервер PostgreSQL за несколько минут, от $20 в месяц. Включены резервные копии, мониторинг, патчи и круглосуточная техническая поддержка.
* [DigitalOcean Managed Databases](https://www.digitalocean.com/products/managed-databases/) - Полностью управляемые базы данных PostgreSQL. Нет бесплатного плана. Начиная с $15/мес. Ежедневные резервные копии с восстановлением на момент времени. Резервные узлы с автоматическим переключением.
* [Google Cloud SQL for PostgreSQL](https://cloud.google.com/sql/docs/postgres/) - Полностью управляемый сервис баз данных, который упрощает настройку, обслуживание, управление и администрирование ваших реляционных баз данных PostgreSQL на платформе Google Cloud.
* [Heroku Postgres](https://elements.heroku.com/addons/heroku-postgresql) - Планы от бесплатного до крупных, управляемые экспертами PostgreSQL. Не требует запуска вашего приложения на Heroku. Бесплатный план включает 10,000 строк, 20 соединений, до двух резервных копий и поддерживает PostGIS.
* [OVHcloud Cloud Databases](https://www.ovhcloud.com/en/public-cloud/databases/) - Высокодоступный, масштабируемый и защищенный PostgreSQL. Ежедневные резервные копии с восстановлением на момент времени, нет привязки, бесплатный входящий и исходящий трафик.
* [Render Managed PostgreSQL](https://render.com/docs/databases) - Безопасный, надежный и полностью управляемый PostgreSQL. Шифрование на уровне хранения, автоматизированные резервные копии и расширяемое SSD-хранилище включены во все планы. Планы начинаются с $7 в месяц за 256MB оперативной памяти и 1GB хранилища (бесплатно в течение первых 90 дней).
* [ScaleGrid PostgreSQL DBaaS](https://scalegrid.io/postgresql.html) - Полностью управляемый хостинг PostgreSQL с высокой доступностью, выделенными серверами и контролем суперпользователя на лучшей мультиоблачной альтернативе Amazon RDS.
* [Scaleway Managed Database](https://www.scaleway.com/en/database/) - Полностью управляемые базы данных PostgreSQL с высокой доступностью, масштабированием и автоматизированными резервными копиями, размещенные в ЕС. Начиная с €10 в месяц.
* [Supabase](https://www.supabase.com) - Полностью управляемый Postgres с репликами для чтения, восстановлением на момент времени, пакетами поддержки, графическим интерфейсом на основе браузера и щедрым бесплатным уровнем.
* [Neon](https://neon.tech) - Полностью управляемый серверный PostgreSQL. Neon разделяет хранилище и вычисления, чтобы предложить современные функции для разработчиков, такие как серверность, ветвление, бездонное хранилище и многое другое.
* [Nile](https://www.thenile.dev/) - Полностью управляемый PostgreSQL. Nile разделяет хранилище и вычисления и виртуализирует арендаторов для быстрой, безопасной и безгранично масштабируемой доставки многопользовательских AI приложений. Бесплатный уровень предоставляет неограниченное количество баз данных.

### Docker образы
* [citusdata/citus](https://hub.docker.com/r/citusdata/citus/) - Официальные образы Citus с расширениями Citus. Основаны на официальном контейнере Postgres.
* [mdillon/postgis](https://hub.docker.com/r/mdillon/postgis/) - PostGIS 2.3 на Postgres 9. Основан на официальном контейнере Postgres.
* [paradedb/paradedb](https://hub.docker.com/r/paradedb/paradedb/) - ParadeDB — это Postgres для поиска и аналитики. Основан на контейнере Bitnami Postgres с расширениями pg_search и pg_analytics для Postgres.
* [postgres](https://hub.docker.com/_/postgres/) - Официальный контейнер postgres (от Docker).

### Kubernetes
* [Crunchy Operator](https://github.com/CrunchyData/postgres-operator) - Production PostgreSQL для Kubernetes, от высокодоступных кластеров Postgres до полноценной базы данных как сервиса.
* [Fujitsu Enterprise Postgres для Kubernetes](https://www.postgresql.fastware.com/) - PostgreSQL корпоративного уровня на платформе OpenShift Container Platform (Коммерческое ПО).
* [Kubegres Operator](https://github.com/reactive-tech/kubegres) - Kubegres — это Kubernetes оператор, позволяющий развертывать один или несколько кластеров экземпляров PostgreSql и управлять репликацией, переключением и резервным копированием баз данных.
* [StackGres Operator](https://github.com/ongres/stackgres/) - Полный стек PostgreSQL на Kubernetes.
* [Zalando Operator](https://github.com/zalando/postgres-operator) - Создает и управляет кластерами PostgreSQL, работающими в Kubernetes.
* [CloudNativePG operator](https://github.com/cloudnative-pg/cloudnative-pg) - Комплексная платформа, предназначенная для беспрепятственного управления базами данных PostgreSQL в средах Kubernetes.
* [KubeDB operator](https://kubedb.com/) - Запуск баз данных производственного уровня на Kubernetes (Коммерческое ПО).

## Ресурсы

### Учебные пособия
* [Tricking Postgres into using an insane – but 200x faster – query plan](https://spacelift.io/blog/tricking-postgres-into-using-query-plan)

### Книги
* [PostgreSQL Mistakes and How to Avoid Them](https://www.manning.com/books/postgresql-mistakes-and-how-to-avoid-them)
* [The Internals of PostgreSQL](https://www.interdb.jp/pg/index.html) - Бесплатная электронная книга от Хиронобу Судзуки
* [PostgreSQL 14 Internals](https://postgrespro.com/community/books/internals) - Бесплатная электронная книга от Егора Рогова

### Документация
* [Wiki](https://wiki.postgresql.org/wiki/Main_Page) - пользовательская документация, руководства и советы
* [pgPedia](https://pgpedia.info/) - Энциклопедия, связанная с PostgreSQL.

### Рассылки
* [Postgres Weekly](https://postgresweekly.com/) - Еженедельная рассылка, содержащая статьи, новости и репозитории, связанные с PostgreSQL.
* [pgMustard newsletter](https://www.pgmustard.com/newsletter) - Ежемесячная рассылка, содержащая статьи и видео о производительности Postgres.

### Подкасты
* [PostgresFM](https://postgres.fm/) - Еженедельные обсуждения на темы Postgres.
* [Scaling Postgres](https://www.scalingpostgres.com/) - Еженедельные подборки контента, связанного с PostgreSQL.
* [Path to Citus Con](https://www.citusdata.com/podcast/path-to-citus-con/) - Ежемесячные интервью с людьми из мира Postgres.

### Видео
* [Citus Data Youtube channel](https://www.youtube.com/channel/UC8jpoK1BqQhDh6HDGFnM_DA/videos) - Видео, связанные с Citus
* [EnterpriseDB Youtube channel](https://www.youtube.com/channel/UCkIPoYyNr1OHgTo0KwE9HJw) - Видео, связанные с EnterpriseDB
* [Postgres Conference Youtube channel](https://www.youtube.com/channel/UCsJkVvxwoM7R9oRbzvUhbPQ/videos) - Видео конференций
* [Scaling Postgres](https://www.scalingpostgres.com/) - Серия видеоблогов о Postgres от Creston Jamison
* [PostgresTV Youtube channel](https://www.youtube.com/@PostgresTV) - Выступления, сессии хакинга, интервью и эпизоды подкастов о Postgres

### Сообщество
* [Mailing lists](https://www.postgresql.org/list/) - Официальные списки рассылки для поддержки Postgres и многого другого. Один из основных каналов связи в сообществе Postgres.
* [Reddit](https://www.reddit.com/r/PostgreSQL/) - Сообщество пользователей PostgreSQL на Reddit с более чем 12000 пользователей
* [Slack](https://pgtreats.info/slack-invite) - Рабочее пространство Slack для Postgres с более чем 20k участников
* Telegram - Несколько групп для PostgreSQL на разных языках: [Русский](https://t.me/pgsql) >4200 человек, [Бразильский португальский](https://t.me/postgresqlbr) >2300 человек, [Индонезийский](https://t.me/postgresql_id) ~1000 человек, [Английский](https://t.me/postgreschat) >750 человек
* [#postgresql на Freenode](https://webchat.freenode.net/#postgresql) - Самый популярный IRC канал о Postgres на Freenode с более чем 1000 пользователей
* [Discord](https://discord.gg/bW2hsax8We) - Сервер Discord для Postgres с более чем 6k участников

### Дорожные карты
* [PostgreSQL Roadmap](https://roadmap.sh/postgresql-dba) - Дорожная карта, предоставляющая пошаговое руководство по PostgreSQL.

### Внешние списки
* [Wikipedia admin tools list](https://en.wikipedia.org/wiki/Comparison_of_database_tools) - Сравнение инструментов администрирования баз данных на Wikipedia
* [PostgreSQL Wiki GUI tools list](https://wiki.postgresql.org/wiki/Community_Guide_to_PostgreSQL_GUI_Tools) - Руководство сообщества по инструментам GUI для PostgreSQL
* [PostgreSQL Wiki Foreign Data Wrappers list](https://wiki.postgresql.org/wiki/Foreign_data_wrappers) - Обертки для внешних данных
