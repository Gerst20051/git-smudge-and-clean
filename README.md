git-smudge-and-clean
====================

Demonstration Of Git Smudge And Clean

Add This To Your Repo Config File

path/to/repo/.git/config

IF YOU WANT TO CONVERT SPACES TO TABS (PUSHING)

[filter "tabs-to-spaces"]
	smudge = unexpand --tabs=4 --first-only
	clean = expand --tabs=4 --initial

IF YOU WANT TO CONVERT TABS TO SPACES (PUSHING)

[filter "spaces-to-tabs"]
	smudge = expand --tabs=4 --first-only
	clean = unexpand --tabs=4 --initial

Add This To Your Attributes Info File

path/to/repo/.git/info/attributes

IF YOU WANT TO CONVERT SPACES TO TABS

*.file_extension filter=spaces-to-tabs

IF YOU WANT TO CONVERT TABS TO SPACES

*.file_extension filter=tabs-to-spaces

