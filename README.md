django-python-telegram-bot-adapter
=====

1. Install django-python-telegram-bot-adapter 
    ``` 
    pip install django-python-telegram-bot-adapter
    ```
2. Add `bot_adapter` to your INSTALLED_APPS setting
    ```python
    INSTALLED_APPS = [
        ...
        'bot_adapter.apps.BotConfig',
    ]
    ```
3. Include URLconf in your project urls.py
    ```python
    path('/', include('bot_adapter.urls')),
    ```
4. Not you can create telegram bots
    ```python
    bot = Bot(TOKEN)
    bot.register(...)
    BotConfig.registry.add_bot(TOKEN, bot)
    ```