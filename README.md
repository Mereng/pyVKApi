# Установка
```
$ git clone git@github.com:Mereng/pyVKApi.git
$ cd pyVKApi
$ python setup.py install
```

# Работа с библиотекой

```python
from pyVK import Api
```
## Авторизация

### Если токен уже получен

```python
api = Api(token, expires_in, user_id)
```
**token** - Собственно токен

**expires_id** - Время жизни токена

**user_id** - ID текущего пользователя

### Получения токена, используя логин и пароль

```python
api = Api()
api.auth(app_id, scope, login, password)
```

**app_id** - ID вашего приложения

**scope** - Разрешения приложения в формате "*messages,audio,groups*"

**login**, **password** - И так понятно

## Вызов методов

```python
response = api.call_method(method, params)
```

**method** - Название метода

**params** - Словарь параметров

Результатом функции будет словарь
