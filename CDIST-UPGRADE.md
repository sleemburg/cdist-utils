# NAME

cdist-upgrade

# SYNOPSIS

`cdist-upgrade`

# DESCRIPTION

A simple wrapper to aid in changing/upgrading cdist version.

The command expects to `CDIST_INSTALL` environment variable to be set and point to
the location where the cdist software is installed (repository checked out).

When the command is run it will generate a list of versions of the cdist software
and present those in a list. The current version will be highlighted. If any other
version is selected, the script will attempt to change the repository to that version
of cdist.

# EXAMPLES

Change to verion 4.0.0 of cdist.

* run `cdist-upgrade`
* Highlight version 4.0.0
* Press enter

# AUTHOR

Written by Mark Verboom

# REPORTING BUGS

Prefferably by opening an issue on the github page.

# COPYRIGHT

Copyright  ©  2014  Free Software Foundation, Inc.  License GPLv3+: GNU
GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
This is free software: you are free  to  change  and  redistribute  it.
There is NO WARRANTY, to the extent permitted by law.
