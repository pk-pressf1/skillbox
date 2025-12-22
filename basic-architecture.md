# Базовая архитектура

## Основные принципы:

- **Событийно-ориентированная модель (Kafka)** как backbone
- **Domain-Driven Design**: каждый сервис — отдельный bounded context
- **Zero Trust Security**: каждый запрос проверяется, данные сегментированы
- **Observability by design**: все компоненты инструментированы (OpenTelemetry)
- **Mobile-first + offline-first**: данные тренировок синхронизируются асинхронно

## Как архитектура закрывает ключевые требования:

- **Социальные группы** → Social Graph Service + Neo4j
- **Сравнение с собой/регионом** → Activity Tracking + аналитика в ClickHouse
- **Инвентарь и рекомендации** → User & Profile + Commerce Adapter
- **Геймификация и промо** → Gamification + Promo Service (управляемые конфигурацией)
- **Приватность** → Auth & Privacy Core с granular consent
- **Масштабируемость** → горизонтальное масштабирование сервисов, партиционирование Kafka
- **Надёжность** → multi-AZ развёртывание, RTO/RPO как SLO
