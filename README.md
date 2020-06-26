# ransomware_rename
Remove unwanted ransomware encryption extensions

## Install homebrew
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`

## Install rename
`brew install rename`

## Change to top level directory
`cd /path/to/dir`

## Check output (optional)
```bash
find . -type f -name '*.AKO' -exec realpath '{}' \;               # prints in terminal
find . -type f -name '*.AKO' -exec realpath '{}' \; > log.txt     # saves log.txt in present working directory
```

## Rename
`find . -type f -name '*.AKO' -exec realpath '{}' \; -exec rename -d ".AKO" {} \;`
