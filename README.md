# Awesome Cloud9
Collection of tips and gotchas, making Cloud IDE great again! My own personal notes collected from the internet.

## Table of Content

- [Python](#python)
- [Node](#node)

## Python

### Setup a new runner with the virtualenv

- Inside c9 in Menu, Run > Run with... > New Runner
- Replace the following:

  _NOTE_: Assume you created virtualenv called `py3`. (ie. `$ virtualenv -p //usr/bin/python3 py3`)
  
  old
  ```
  {
      "cmd" : ["ls", "$file", "$args"],
      "info" : "Started $project_path$file_name",
      "env" : {},
      "selector" : "source.ext"
  }
  ```
  
  For Flask
  ```
  {
      "cmd": [
          "bash",
          "--login",
          "-c",
          "source ./py3/bin/activate && python your_mad_script.py"
      ],
      "working_dir": "$project_path",
      "info": "Your code is running at \\033[01;34m$url\\033[00m.\n\\033[01;31m"
  }
  ```
  
  For Django
  ```
  {
      "cmd": [
          "bash",
          "--login",
          "-c",
          "source bin/activate && cd django_root_project && python manage.py runserver $ip:$port"
      ],
      "working_dir": "$project_path",
      "info": "Your code is running at \\033[01;34m$url\\033[00m.\n\\033[01;31m"
  }
  ```
- Save your runner with a clever name. (ie. `virtualenv_py3.runner`)
- Enjoy!
- Appendix
  - [ref](https://community.c9.io/t/configuring-a-runner-with-virtualenv/16717), [ref](https://docs.c9.io/docs/custom-runners), [ref](https://docs.c9.io/docs/custom-runners#section-django)

## Node

- TODO

### 
