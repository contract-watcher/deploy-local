# ContractWatcher Infrastructure

Репозиторий с общей локальной инфраструктурой ContractWatcher.

## Запуск

Подтянуть актуальные образы и поднять сервисы:

```bash
docker compose pull && docker compose up -d
```

## Перезапуск с обновлением образов

```bash
docker compose pull && docker compose up -d --force-recreate
```

## Остановка

```bash
docker compose down
```

## Полный сброс

Удалит контейнеры вместе с volume PostgreSQL:

```bash
docker compose down -v
```

## Запуск тестового апи

Необходимо прописать апи ключ в переменную `IntegrationKey` и собрать контейнер

```bash
docker compose -f test-api-compose.yml up -d --force-recreate
```