# ZEIT ONLINE Python Coding Guidelines

Please read and adhere to [PEP 8](http://legacy.python.org/dev/peps/pep-0008/).

The following additional guidelines are structured according to the original
PEP 8 document.

## Maximum Line Length

If the first argument is on the same line as the opening bracket, close it
inline and indent sufficiently.

```Python
foo = package.module.very_long_variable_name(this_is_argument_one, second_arg
                                             first_keyword=None, second_kw=17)
```

If the arguments are live on separate lines, put the closing bracket on a
separate line, as well.

```Python
foo = package.module.some_method(
    bar.content,
    'foo-layout',
    kwarg1='bar',
    kwarg2=False
)
```

Avoid breaking long lines using backslashes. Instead, use brackets.
Note, that Python implicitly joins strings that are contained in brackets.

```Python
assert ('<html><body><div><h1>{{ title }}</h1>'
        '<div class="container">{{ content }}</div>'
        '</div></body></html>') in foo.contents
```

## Imports

In addition to the suggested PEP 8 import order, use a fourth section to group
import statements.

* standard library imports
* third party imports
* zeit namespace imports
* project specific imports

You should put a blank line between each group of imports. You should also
import full paths rather than importing explicitly using the `from` statement.

```Python
import base64
import sys

import pyramid
import jinja2.runtime

import zeit.some.project
import zeit.other.project

import zeit.scope.project.module


app = zeit.scope.project.module.app_factory()
```
