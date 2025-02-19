# Project Creation Prompts

## Initial prompt

```
I need a python fastapi application with a single hello world endpoint. Please use uv as a package manager. I'll need unit tests with pytest as well.

It should be built using docker.

Can you also add the github workflows for building and linting with ruff?

Can you also add the deployment to digital ocean via a container registry at digital ocean

Can you add a README.md with all the usual project information

please use python 3.13, and deploy to Digital Ocean's app platform instead of DOKS

can you use pyproject.toml instead of uv.json?

make sure that the pyproject.toml has a [project] section

make sure that you add the requires-python line in the pyproject.toml
```

## Prompt #2

```
problem:

Traceback (most recent call last):
File "/Users/peter/.local/share/uv/python/cpython-3.13.0-macos-x86_64-none/lib/python3.13/multiprocessing/process.py", line 313, in _bootstrap
self.run()
~~~~~~~~^^
File "/Users/peter/.local/share/uv/python/cpython-3.13.0-macos-x86_64-none/lib/python3.13/multiprocessing/process.py", line 108, in run
self._target(*self._args, **self._kwargs)
~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/_subprocess.py", line 80, in subprocess_started
target(sockets=sockets)
~~~~~~^^^^^^^^^^^^^^^^^
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/server.py", line 66, in run
return asyncio.run(self.serve(sockets=sockets))
~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/Users/peter/.local/share/uv/python/cpython-3.13.0-macos-x86_64-none/lib/python3.13/asyncio/runners.py", line 194, in run
return runner.run(main)
~~~~~~~~~~^^^^^^
File "/Users/peter/.local/share/uv/python/cpython-3.13.0-macos-x86_64-none/lib/python3.13/asyncio/runners.py", line 118, in run
return self._loop.run_until_complete(task)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^
File "/Users/peter/.local/share/uv/python/cpython-3.13.0-macos-x86_64-none/lib/python3.13/asyncio/base_events.py", line 721, in run_until_complete
return future.result()
~~~~~~~~~~~~~^^
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/server.py", line 70, in serve
await self._serve(sockets)
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/server.py", line 77, in _serve
config.load()
~~~~~~~~~~~^^
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/config.py", line 435, in load
self.loaded_app = import_from_string(self.app)
~~~~~~~~~~~~~~~~~~^^^^^^^^^^
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/importer.py", line 22, in import_from_string
raise exc from None
File "/Users/peter/dev/fastapi-cline-anthropic/.venv/lib/python3.13/site-packages/uvicorn/importer.py", line 19, in import_from_string
module = importlib.import_module(module_str)
File "/Users/peter/.local/share/uv/python/cpython-3.13.0-macos-x86_64-none/lib/python3.13/importlib/__init__.py", line 88, in import_module
return _bootstrap._gcd_import(name[level:], package, level)
~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "<frozen importlib._bootstrap>", line 1387, in _gcd_import
File "<frozen importlib._bootstrap>", line 1360, in _find_and_load
File "<frozen importlib._bootstrap>", line 1310, in _find_and_load_unlocked
File "<frozen importlib._bootstrap>", line 488, in _call_with_frames_removed
File "<frozen importlib._bootstrap>", line 1387, in _gcd_import
File "<frozen importlib._bootstrap>", line 1360, in _find_and_load
File "<frozen importlib._bootstrap>", line 1324, in _find_and_load_unlocked
ModuleNotFoundError: No module named 'app'
```

