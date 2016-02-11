```sh
$ defaults write some.editor.Application WebKitDeveloperExtras -bool true
```

or for all apps

```sh
$ defaults write -GlobalDomain WebKitDeveloperExtras -bool true
```

or

```sh
$ defaults write NSGlobalDomain WebKitDeveloperExtras -bool true
```
But don’t anymore with iTunes and App Store since OS X 10.8
