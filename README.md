# Telebridge

![demonstration](https://github.com/cyborg-ubyvtsya/telegram-mastodon-bridge/blob/main/img/demo.gif)

Telegram/Mastodon bot for forwarding messages.

## Usage

- [Create a telegram bot](https://core.telegram.org/bots#3-how-do-i-create-a-bot)
- - Recieve telegram's access token
- [Create a mastodon bot](https://tinysubversions.com/notes/mastodon-bot/)
- - Give it the rights to write statuses
- - Save mastodon's access token
- Add your Telegram bot to the channels you need as admin
- Clone the repo
- Install `Docker` and `docker-compose`
- Add a `.env` file with this env vars:
  - `MASTODON_TOKEN=Your_Mastodon_access_token`
  - `TELEGRAM_TOKEN=Your_Telegram_token`
  - `MASTODON_INSTANCE=https://yourinstance.social`
  - `MASTODON_VISIBILITY=public`
  - `MASTODON_CHARACTER_LIMIT=500`
- Run the bot: `docker-compose up --build -d`
- Bot will start forwarding posts


## Modifications

There's no footer message.

### Limitations

- Only reposts plain text(mastodon limitation), images, and videos
- Image galleries are published as separate posts(telebot library limitation)

## References

- [Telegram bot API documentation](https://pypi.org/project/pyTelegramBotAPI/)
- [Mastodon bot API documentation](https://mastodonpy.readthedocs.io/en/stable/)
