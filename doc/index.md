# Droidhub.net Home Page

The Droidhub.net project aims to enhance sharing of Free Open Source Software
(FOSS) among Android application developers.  If you have a package to share,
or want to help get Droidhub.net started, join the [Github Google
group](http://groups.google.com/group/droidhub) and introduce yourself.

## Tools

The primary tool will be 'droid', which will allow you to search for packages,
install and uninstall them in your application directory, deal with
dependencies, create your own packages, and publish them.  Supported commands
are projected to include (courtesy of Doug in the Droidhub Google group):

\# Install a package from a repository (droidhub.net by default)
droid install [name] [path/to/app]

\# Install a package manually
droid install [path/to/src] [path/to/app]

\# Search the packages for relevant info
droid search [keywords]

\# List all available packages
droid list

\# Fetch and display the info about a package.
droid list [name]

\# Run wizard to create droidhub package directory
droid init

\# Upload your package to the target repository (defaults to droidhub.net)
droid publish [target]

\# Add a new repository
droid repo-add [URL]

\# Remove a repository
droid repo-remove [URL]

\# List repos
droid repo-list
