# ransomware_rename
Remove unwanted ransomware encryption extensions

## Install homebrew
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`

## Install rename
`brew install rename`

## Change to top level directory
`cd /path/to/dir`

## Check output (optional)
`find . -type f -name '*.AKO' -exec realpath '{}' \;`

## Rename
`find . -type f -name '*.AKO' -exec realpath '{}' \; -exec rename -d ".AKO" {} \;`
