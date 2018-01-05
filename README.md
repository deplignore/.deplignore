# .deplignore
.gitignore-inspired convention for defining files, that should never be uploaded.

## Conventions

1. A `.deplignore` placed into a directory, matches files in that directory and it's child-directories.
1. Files matching the `.deplignore`s rules, should be omitted when uploading the directories content to a server. I.E.: Those files are, at no point in time, going over the network.
1. `.deplignore` is plaintext UTF-8
1. One line is one rule
1. Empty lines and lines starting with a `#` are not considered a rule
1. Lines starting with a `!` define exceptions for previous rules

**TLDR:** Everything behaves just like in a `.gitignore`

## Examples

```.gitignore
# This is a comment

# This matches all files which are named exactly foo.bar (anywhere in path)
foo.bar

# This matches all files with the extension .bar
*.bar

# Except they are named test.bar
!test.bar

# This matches files which are named exactly baz.baz, but only in the current directory
/baz.baz

# Matches files and directorys which are named bazinga
bazinga

# Matches only directories which are named sonicScrewdriver
sonicScrewdriver/

# Matches all files which are named test and listed anywhere under foo, no matter how many dirs are between them
foo/**/test
```

## Known software-support

If you know FTP-Clients, Build-servers, deployment-tools or anything else, that supports this, let us know!
