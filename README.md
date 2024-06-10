<p align="center">
    <a href="github.address">
        <img src="https://raw.githubusercontent.com/irvanyamirali/aiorubika/master/icon.png" alt="AIORubika" width="128">
    </a>
    <br>
    <b>Rubika API Framework for Python</b>
    <br>
    <a href="https://github.com/irvanyamirali/aiorubika">
        Homepage
    </a>
    •
    <a href="https://github.com/irvanyamirali/aiorubika">
        Documentation
    </a>
    •
    <a href="https://pypi.org/project/aiorubika/#history">
        Releases
    </a>
</p>

## AIORubika

> Elegant, modern and asynchronous Rubika API framework in Python for users and bots

### Async Accounts
```python
from aiorubika import Client, filters, utils
from aiorubika.types import Updates

bot = Client(name='my_account')

@bot.on_message_updates(filters.text)
async def updates(update: Updates):
    print(update)
    await update.reply(utils.Code('hello') + utils.Underline('from') + utils.Bold('aiorubika'))

bot.run()
```

**Async Another Example:**
```python
from aiorubika import Client
import asyncio

async def main():
    async with Client(name='my_account') as bot:
        result = await bot.send_message('me', '`hello` __from__ **aiorubika**')
        print(result)

asyncio.run(main())
```

### Sync Accounts
```python
from aiorubika import Client

bot = Client('my_account')

@bot.on_message_updates()
def updates(message):
    message.reply('`hello` __from__ **aiorubika**')

bot.run()
```

**Sync Another Example:**
```python
from aiorubika import Client

with Client(name='my_account') as client:
    result = client.send_message('me', '`hello` __from__ **aiorubika**')
    print(result)
```

**AIORubika** is a modern, elegant and asynchronous framework. It enables you to easily interact with the main Rubika API through a user account (custom client) or a bot
identity (bot API alternative) using Python.


### Key Features

- **Ready**: Install AIORubika with pip and start building your applications right away.
- **Easy**: Makes the Rubika API simple and intuitive, while still allowing advanced usages.
- **Elegant**: Low-level details are abstracted and re-presented in a more convenient way.
- **Fast**: Boosted up by pycryptodome, a high-performance cryptography library written in C.
- **Async**: Fully asynchronous (also usable synchronously if wanted, for convenience).
- **Powerful**: Full access to Rubika's API to execute any official client action and more.

### Installing

``` bash
pip3 install -U aiorubika
```
