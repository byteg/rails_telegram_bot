# Rails Telegram Bot

Отправка сообщения через бота Телеграма из Рельс.

## Как запускать
Устанавливаем redis, запускаем его, создаем в директории проекта файл `.env` и прописываем в него:

```
TELEGRAM_BOT_CHANNEL='идентификатор канала'
TELEGRAM_BOT_TOKEN='токен бота'
```

запускаем `rails s`, в другой консоли запускаем `sidekiq` (из директории с рельсовым проектом).

## Как узнать идентификатор канала
Отправляем сообщение боту через Телеграм, заходим по адресу `https://api.telegram.org/botВСТАВЬ_СЮДА_ТОКЕН_БОТА/getUpdates?offset=0` и смотрим `result → message → chat → id`.


## P.S.
На данный момент через бота сообщения можно отправлять только лично пользователю, на канал нельзя.