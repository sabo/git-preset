git-preset
=====

Manage git configuration presets.

Example
-----
```
$ git init # Set up a new repository
Initialized empty Git repository in <redacted>/test/.git/
$ git config --get user.email # hasn't been set locally, so comes from global or system
sabo@lattid.com
$ git preset work # This is for a project for work
--> Setting user.signingkey to <redacted>
--> Setting user.email to gsablosky@bard.edu
$ git config --get user.email # ta-da
gsablosky@bard.edu
```

Options
-----
|Flag|Effect|
|---|---|
|-f, --filter `regex`|Only apply or save keys that match `regex`|
|-s, --save-preset `name`|Save local config as new preset `name`|
|-c, --clobber|When saving, overwrite the preset if it exists|
|-d, --dry-run|Don't actually apply settings, just display|
|--preset-dir|Location of presets (default: $HOME/.config/git-preset)|
