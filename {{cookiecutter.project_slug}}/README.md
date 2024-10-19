{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}

# {{ cookiecutter.project_name }}

{% if is_open_source %}
[![pypi](https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}.svg)](https://pypi.org/project{{ cookiecutter.project_slug }}/)
[![travis](https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg)](https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug  }})
[![docs](https://readthedocs.org/projects/{{ cookiecutter.project_slug | replace("\*", "-") }}/badge/?version=latest)](https://{{ cookiecutter.project_slug | replace("*", "-") }}.readthedocs.io/en/latest/?badge=latest)

{%- endif %}

{% if cookiecutter.add_pyup_badge == 'y' %}

[![pyup](<https://pyup.io/repos/github>/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/shield.svg)](https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/)

{% endif %}

{{ cookiecutter.project_short_description }}

{% if is_open_source %}

-   Free software: {{ cookiecutter.open_source_license }}
-   Documentation: <https:/>/{{ cookiecutter.project_slug | replace("\_", "-") }}.readthedocs.io.

{% endif %}

## Features

-   TODO

## Credits

This package was created with [Cookiecutter] and the [briggySmalls/cookiecutter-pypackage] project template.

[briggysmalls/cookiecutter-pypackage]: https://github.com/briggySmalls/cookiecutter-pypackage
[cookiecutter]: https://github.com/audreyr/cookiecutter
