Git Changelog Generator for Assembla (git-clog)
===============================================

Helps prepare a changelog for the changes between two commits.

The changelog can be output as an excerpt from the git log messages, affected Assembla tickets, or the related Assembla merge requests.

See `git-clog -h` for usage information.

Examples
--------
Prints a list of changes since the last tag:

    git-clog

Prints a list of tickets impacted between bug/1234 and master:

    git-clog -o tickets bug/1234..master

Prints URLs of tickets impacted between two specific commits:

    git-clog -o urls 90bb49b..be98809

Tips
----
Output the list of changes in a markdown-suitable format:

    git-clog -o changes tag_name..master | sed 's/^/* /'

If this script is placed in your `$PATH`, you can access it as a git subcommand.

    git clog
