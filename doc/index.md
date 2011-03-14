# Droidhub.net Home Page

The Droidhub.net project aims to enhance sharing of Free/Open Source Software
(FOSS) among Android application developers.  If you have a package to share,
or want to help get Droidhub.net started, join the [Droidhub Google
group](http://groups.google.com/group/droidhub) and introduce yourself.

This page is a simply a road map for where we want the Droidhub.net project to go.  It will be probably several months before the site has live project repositories.

## Enhanced Sharing

Today, sharing FOSS software is far more difficult than it should be.  It literally takes years from the day I create a free software library, to the time that you can easily link to it on your Debian Stable machine, and that's only if I'm lucky enough to attract a sponsor for the library.  If I find a bug in a core package like Firefox or GTK+, it is very difficult to get those bug fixes included, and even if they are, it might be years before most users have access to the fix.

With Android, you go straight to the App Store, with almost no red tape.  However, if you want to include an mp3 decoder, you have to port one yourself, or find someone else's port on the Internet.  With the Droidhub.net project, we will enable Android developers to share their free software in the form of pre-compiled packages, so reusing someone's mp3 port will be simple.  Further, we will enable anyone to fork any package and publish their changes immediately.  Upstream authors can at their convenience pull changes you make, without any effort required by you.

Several innovations are key to enhanced sharing.  First, Android runs all applications in an app jail, which limits the authority your app has to modify other app's data or access hardware.  That enables Google to reduce the time to review a new app to almost zero.  Second, every app ships with every library they use, and they are never updated.  While this causes app bloat and some security issues, it eliminates [Dependency Hell](http://en.wikipedia.org/wiki/Dependency_hell).  In comparison, Debian has to migrate new packages from Unstable to Stable over multiple years, in an effort to insure that upgrading a package wont break anything.  To reduce app bloat, we may use a system like [Ministro](https://market.android.com/details?id=eu.licentia.necessitas.ministro).  However, apps will never have their dependent libraries updated, unless there is a major security problem.  Using a model similar to github.net, any user will be able to fork and publish changes to any package with minimal effort and no delay.  To help users decide which fork of a package to use, a trust system will help users to determine which package forks are trustworthy.

## Tools

To make sharing code as simple as possible, the Droidhub.net web site will
automate publishing your package with a simple form you fill out.  However, you
will also be able to do it from the command line.  The primary tool will be 'droid',
which will allow you to search for packages, install and uninstall them in your
application directory, deal with dependencies, create your own packages, and
publish them.  Supported commands are projected to include (thanks in part to
Doug in the Droidhub Google group):

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

\# Fork an existing package, so you can read the code, modify it and publish  
\# changes.  this creates a git repository of the package locally.  
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
