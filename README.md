# Gammu SMS Gateway

Система для отправки и приёма SMS через несколько USB-модемов. Работает на базе Gammu и PostgreSQL.

## Состав

- PostgreSQL — база для хранения SMS
- Несколько контейнеров Gammu — по одному на каждый модем
- Скрипт обработки входящих сообщений

## Развёртывание через Portainer

1. Добавьте новый **Stack** в Portainer
2. Выберите **Git repository**
3. Укажите:
   - URL: https://gitlab.com/your-user/gammu-sms-gateway.git
   - Path: `docker-compose.yml`
4. Deploy

## Конфигурация

Файл конфигурации для каждого модема находится в `configs/gammu_modem_X/gammu-smsdrc`.

Скрипт обработки входящих сообщений: `scripts/on-receive.sh`
