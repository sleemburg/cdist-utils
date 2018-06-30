# cdist-utils

This is a small collection of scripts I use in combination with cdist to make my
life a bit easier :)

The scripts assume some settings that need to be available in order to function
properly. I set them in the cdist user's environment.

CDIST_INSTALL=path_to_cdist_install

The directory where cdist is installed.

CDISTEXPLORE=path_to_explore_output

The directory where explorer output is stored.

## Components

The following components can be found in this repository:

### runcdist

Wrapper around cdist to make it easier to run cdist.

### cdist-upgrade

Wrapper around some git commands to make it easier to change versions/upgrade.

### cdist-inventory

Create a cdist inventory based on explorer output.
