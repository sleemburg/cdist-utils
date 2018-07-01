# NAME

runcdist

# SYNOPSIS

`runcdist [OPTION]... [HOST]...`

# DESCRIPTION

A wrapper around the cdist software to make running cdist easier. This wrapper
relies on the inventory function of cdist.

Arguments that can be used are:

`-v`
Make output more verbose. Each `-v` increases the verbosity.

`-q`
Make output quiet.

`-p`
Run the configuration of hosts in parallel.

`-o <manifest>`
Overrule running any generic manifest and only run the specified manifest.

`-t <tags..>`
Run manifest(s) on all hosts matching the specified tag(s).

`-a`
Run manifest(s) on all hosts in inventory.

EXAMPLES

Run cdist for all systems tagged as server

`runcdist -t server`

Run cdist with the exim manifest on all systems tagged as mailer and be verbose.

`rundist -v -o exim -t mailer`

# AUTHOR

Written by Mark Verboom

# REPORTING BUGS

Prefferably by opening an issue on the github page.

# COPYRIGHT

Copyright  ©  2014  Free Software Foundation, Inc.  License GPLv3+: GNU
GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
This is free software: you are free  to  change  and  redistribute  it.
There is NO WARRANTY, to the extent permitted by law.
