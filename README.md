# Django-Rest-Framework RBAC plus

**Based on the django USER model, a permission system based on RBAC mode is implemented, 
which provides a background admin entry mechanism for permission, 
and implements permission control with drf middleware.**

---


# Requirements

- Python (3.5+)
- Django (2.1+)

I **highly recommend** and only officially support the latest patch release of each Python and Django series.
# Installation
Install using pip...

```
pip install drf-rbac-plus
```

Add 'drf_rbac' to your INSTALLED_APPS setting.

```
INSTALLED_APPS = [
    ...
    'drf_rbac',
]
```

Add path to your URL setting.

```
urlpatterns = [
    ...
    path('drf_rbac/', include('drf_rbac.urls')),
]
```

Add UserRolePermission to your DEFAULT_PERMISSION_CLASSES(django-restframework setting).

```
    'DEFAULT_PERMISSION_CLASSES': (
        ...
        'drf_rbac.authorization.UserRolePermission',
    ),
```
