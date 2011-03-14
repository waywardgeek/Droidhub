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
droid install name[:version]

\# Install a package manually  
droid install path/to/src

\# Search the packages for relevant info  
droid search keyword...

\# Fetch and display the info about packages.  
\# With no name, list all available packages  
\# With no version, show all forks of a package, sorted by trust.  
droid list [name[:version]]

\# Run wizard to create droidhub package directory  
droid init

\# Fork an existing package, so you can modify it and publish changes  
droid fork name[:version] [dest dir]

\# Upload your package to the target repository (defaults to droidhub.net)  
droid publish [target]

\# Compare your package to another published version of it.  
droid diff [version]

\# Compare two versions of a package.  
droid diff name version1 version2

\# Declare that you trust an author or his package  
droid trust username [packagename]

\# Remove trust for an author or package  
droid stop-trusting username [packagename]

\# Declare that you find an author or package untrustworthy  
droid untrustworthy username [packagename]

\# List your trust relationships  
droid showtrust

\# Add a new repository  
droid repo-add [URL]

\# Remove a repository  
droid repo-remove [URL]

\# List repos  
droid repo-list
