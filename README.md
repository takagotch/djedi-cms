### djedi-cms
---
https://github.com/5monkeys/djedi-cms

http://djedi-cms.org/

```py
INSTALLED_APPS = (
  'djedi',
)

MIDDLEWARE = [
  'djedi.middleware.translation.DjediTranslationMiddleware',
]

urlpatterns = [
  path('admin/', admin.site.urls),
]

{% load djedi_tags %}
<body>
  <h1>{% node 'page/title.txt' defaut='Djedi' %}</h1>
  {% blocknode 'page/body.md' %}
    This is fun!
  {% endblocknode %}
</body>
```

```sh
pip install djedi-cms
django-admin.py migrate djedi

```

```
```


