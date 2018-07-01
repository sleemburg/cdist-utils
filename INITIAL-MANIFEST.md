# NAME

initial-manifest

# DESCRIPTION

This is an example of an initial manifest I use. It works pretty well for me and
might be of use to others.

The initial manifest tries to handle two things:

* Processing explorer output
* Running other manifests

# EXPLORER OUTPUT

Output from the main explorer is often used further in manifests. So it makes sense
to create environment variables for the explorer information, not every manifest
needs to do this itself. This is the first part of of the initial manifest.

The second step is to save the explorer output. In order to do this, two variables
are important:

`CDIST_EXPLORE`
This is an environment variable pointing to a directory that will be used to save
the explore output for all systems. This should be default set in the environment
so other scripts can make use of this.

`fqdn`
This is the fully qualified domain name of the system cdist is configuring at the
moment. When controlling different groups of systems, it is important to get the
fqdn so no nameclashes occur. The fqdn is used to create the directory in the
CDIST_EXPLORE directory for the host.

If a directory already exists for the host it is removed and recreated. This ensures
any old or decommisioned explore information is removed. Then all current explore
output is copied to the directory.

It can be useful after a cdist run or at a specific recurring time, to commit the
explore directory to a version control system. Depending on the type of information
your explore output provides it can help in determining the point at which changes
have occured.

After the explore information is handled, manifests are run. It is not always
optimal to run every manifest for a host. So the `runcdist` script provides an
envirionment variable `CDISTACTION` which if set points to a specific manifest
to be run. If this is the case only this manifest is run.
One exception is the value none. If `CDISTACTION` is set to none, no manifest
is run. This can be useful if only the explorer output needs to be updated.

If the `CDISTACTION` variable isn't set, generic manifests are sourced. I prefer
to keep things split out so I don't have to edit the initial manifest, but it
is an option to include multiple manifests in the initial one.

# AUTHOR

Written by Mark Verboom

# REPORTING BUGS

Prefferably by opening an issue on the github page.

# COPYRIGHT

Copyright  ©  2014  Free Software Foundation, Inc.  License GPLv3+: GNU
GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
This is free software: you are free  to  change  and  redistribute  it.
There is NO WARRANTY, to the extent permitted by law.
