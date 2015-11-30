# WebInfoLab_SearchEngine
A demo tiny Search Engine implemented using Jieba+Whoosh+Django+Django-haystack
It seperates to two sides: backend(Jieba+Whoosh) and frontend(Django/haystack),so we go ahead respectively.
##DjangoFramework
```
django-admin startproject SearchEngine
python manage.py startapp SE
```
add app SE to INSTALLED_APP in setting.py

###URL and View Config
```python
SE/urls.py
from django.conf.urls import url

from . import views

urlpatterns = [
    url(r'^$', views.index, name='index'),
]
```
add `url(r'^SE/', include('SE.urls')),` to `SE/urls.py`

