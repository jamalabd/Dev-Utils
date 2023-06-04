# Dev-Utils

I created Dev-Utils for housing all those utilities and snippets we use in our day-to-day as software developers. From VS code configurations to customizations on your Mac. Contributions are always welcome!

## Mac Maintenance

### Removing unused node modules from a folder

Find Node Modules.
``` 
find . -name "node_modules" -type d -prune -print | xargs du -chs
```

Remove Node Modules. 
``` 
find . -name 'node_modules' -type d -prune -print -exec rm -rf '{}' \;
```
Done!👏🏽
