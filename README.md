Build a container from a recipe:
```bash
sudo singularity build foo_container.img foo_recipe.def
```

Creating a recipe from scratch:
```bash
# Create a sandbox image from base ubuntu image
sudo singularity build --sandbox  foo_container shub://singularityhub/ubuntu:latest

# Shell into the sandbox image
sudo singularity shell --writable foo_container

# Setup the sandbox and keep track of the relevant commands in a recipe
.
.
.

# Once you have successfully setup the sandbox, you should also have
# a working recipe which you can then use to build container images
