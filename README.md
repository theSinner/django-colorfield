[![](https://img.shields.io/pypi/pyversions/django-colorfield.svg?color=3776AB&logo=python&logoColor=white)](https://www.python.org/)
[![](https://img.shields.io/pypi/djversions/django-colorfield?color=0C4B33&logo=django&logoColor=white&label=django)](https://www.djangoproject.com/)

[![](https://img.shields.io/pypi/v/django-colorfield.svg?color=blue&logo=pypi&logoColor=white)](https://pypi.org/project/django-colorfield/)
[![](https://pepy.tech/badge/django-colorfield)](https://pepy.tech/project/django-colorfield)
[![](https://img.shields.io/github/stars/fabiocaccamo/django-colorfield?logo=github)](https://github.com/fabiocaccamo/django-colorfield/)
[![](https://badges.pufler.dev/visits/fabiocaccamo/django-colorfield?label=visitors&color=blue)](https://badges.pufler.dev)
[![](https://img.shields.io/pypi/l/django-colorfield.svg?color=blue)](https://github.com/fabiocaccamo/django-colorfield/blob/master/LICENSE.txt)

[![](https://img.shields.io/travis/fabiocaccamo/django-colorfield?logo=travis&label=build)](https://travis-ci.org/fabiocaccamo/django-colorfield)
[![](https://img.shields.io/codecov/c/gh/fabiocaccamo/django-colorfield?logo=codecov)](https://codecov.io/gh/fabiocaccamo/django-colorfield)
[![](https://img.shields.io/codacy/grade/194566618f424a819ce43450ea0af081?logo=codacy)](https://www.codacy.com/app/fabiocaccamo/django-colorfield)
[![](https://img.shields.io/codeclimate/maintainability/fabiocaccamo/django-colorfield?logo=code-climate)](https://codeclimate.com/github/fabiocaccamo/django-colorfield/)
[![](https://requires.io/github/fabiocaccamo/django-colorfield/requirements.svg?branch=master)](https://requires.io/github/fabiocaccamo/django-colorfield/requirements/?branch=master)

# django-colorfield
simple color field for your models with a nice color-picker in the admin-interface.

![django-colorfield](https://user-images.githubusercontent.com/1035294/74674565-f33ace00-51b1-11ea-8669-4b952f2b8e56.png)

## Installation
-   Run `pip install django-colorfield`
-   Add `colorfield` to `settings.INSTALLED_APPS`
-   Run `python manage.py collectstatic`
-   Restart your application server

## Usage

### Settings
This package doesn't need any setting.

### Models
Just add color field(s) to your models like this:

```python
from colorfield.fields import ColorField
from django.db import models

class MyModel(model.Model):
    color = ColorField(default='#FF0000')
```

### Admin
The admin will kindly provide a simple [color picker](http://jscolor.com/) for all color fields. :)

## Testing
```bash
# create python virtual environment
virtualenv testing_django_colorfield

# activate virtualenv
cd testing_django_colorfield && . bin/activate

# clone repo
git clone https://github.com/fabiocaccamo/django-colorfield.git src && cd src

# install dev requirements
pip install -r requirements.txt

# run tests
tox
# or
python setup.py test
# or
python -m django test --settings "tests.settings"
```

## Credits
Originally developed by [Jared Forsyth](https://github.com/jaredly)

## License
Released under [MIT License](LICENSE.txt).

---

## See also

- [`django-admin-interface`](https://github.com/fabiocaccamo/django-admin-interface) - the default admin interface made customizable by the admin itself. popup windows replaced by modals. 🧙 ⚡

- [`django-extra-settings`](https://github.com/fabiocaccamo/django-extra-settings) - config and manage typed extra settings using just the django admin. ⚙️

- [`django-maintenance-mode`](https://github.com/fabiocaccamo/django-maintenance-mode) - shows a 503 error page when maintenance-mode is on. 🚧 🛠️

- [`django-redirects`](https://github.com/fabiocaccamo/django-redirects) - redirects with full control. ↪️

- [`django-treenode`](https://github.com/fabiocaccamo/django-treenode) - probably the best abstract model / admin for your tree based stuff. 🌳

- [`python-benedict`](https://github.com/fabiocaccamo/python-benedict) - dict subclass with keylist/keypath support, I/O shortcuts (base64, csv, json, pickle, plist, query-string, toml, xml, yaml) and many utilities. 📘

- [`python-codicefiscale`](https://github.com/fabiocaccamo/python-codicefiscale) - encode/decode Italian fiscal codes - codifica/decodifica del Codice Fiscale. 🇮🇹 💳

- [`python-fsutil`](https://github.com/fabiocaccamo/python-fsutil) - file-system utilities for lazy devs. 🧟‍♂️
