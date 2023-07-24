# Dev Environments

This project contains several docker images that can be used to set up vanilla lightweight development environments.

## Several tips

Several tips to keep your docker images small:

- Use a lightweight base image, such as Alpine.

Several tips to keep your docker images fast:

- Docker has a layered structure. The more layers you have, the slower it is to build. Try to combine commands into one layer.
- Docker builds its images from the most central layer to the most peripheral layer. Try to put the most frequently changing commands at the end of the Dockerfile. This speeds up image rebuilds.
- Docker has its own caching mechanism. Try running install commands with a `--no-cache` flag or option. This speeds up image rebuilds.

Several tips to keep your docker images secure:

- Do not run as root. Use the `USER` directive to switch to a non-root user.
- Do not install unnecessary packages. Use the `--no-install-recommends` flag when installing packages.

Other tips can be found [here](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/).
