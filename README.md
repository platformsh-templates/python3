> [!WARNING]
> **This repository is no longer maintained by our internal teams.**  
> The template is provided *as is* and will not receive updates, bug fixes, or new features.  
> You are welcome to contribute on it or fork the repository and modify it for your own use.
> To deploy this template on [Upsun](https://www.upsun.com), you can use the command [upsun project:convert](https://docs.upsun.com/administration/cli/reference.html#projectconvert)
> on this codebase to convert the existing `.platform.app.yaml` configuration file to the [Upsun Flex format](https://docs.upsun.com/create-apps/app-reference/single-runtime-image.html).

# Basic Python 3 for Platform.sh

This template provides the most basic configuration for running a custom Python 3.7 project.  It includes the `platformshconfig` package and demonstrates using it to connect to MariaDB and Redis.  It can be used to build a very rudimentary application but is intended primarily as a documentation reference.  The application starts as a bare Python process with no separate runner.

Python is a general purpose scripting language often used in web development.

## Features

* Python 3.8
* MariaDB 10.4
* Redis 5.0
* Automatic TLS certificates
* Pipfile-based build

## Customizations

The following files are of particular importance.  If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.

## Running locally

The `server.py` script expects to find which port to use through a `PORT` environment variable.
Platform.sh provides one automatically.
To replicate the experience locally, start the server with a command like the following (use any port that you like):

```bash
PORT=8000 python server.py
```

## References

* [Python](https://www.python.org/)
* [Python on Platform.sh](https://docs.platform.sh/languages/python.html)
