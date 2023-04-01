### Hi there 👋

🔭 I’m currently working on [aioauth - Asynchronous OAuth 2.0 framework for Python 3](https://github.com/aliev/aioauth)

🔭 I’m currently working on [aioauth-fastapi](https://github.com/aliev/aioauth-fastapi) demo server

🤔 I’m looking for help with [documenting aioauth](https://github.com/aliev/aioauth)

---

🔭 I created new library - [aioshutdown](https://github.com/aliev/aioshutdown) the context manager that provides simple graceful shutdown interface for your asyncio tasks.

Usage example:

```python
import asyncio
from aioshutdown import SIGTERM, SIGINT, SIGHUP


async def my_task(sleep: int):
    try:
        ...
    except asyncio.CancelledError as exc:
        # Your graceful shutdown logic here


# The list of the signals, that you want to handle
with SIGTERM | SIGHUP | SIGINT as loop:
    # The list of your tasks
    tasks = [loop.create_task(my_task(i)) for i in range(1, 10)]
    loop.run_forever()
```
