# Dev-Utils

I created Dev-Utils for housing all those utilities and snippets we use in our day-to-day as software developers. From VS code configurations to customizations on your Mac. Contributions are always welcome!

## Mac

### Maintenance

#### Removing unused node modules from a folder

Find Node Modules.
``` 
find . -name "node_modules" -type d -prune -print | xargs du -chs
```

Remove Node Modules. 
``` 
find . -name 'node_modules' -type d -prune -print -exec rm -rf '{}' \;
```
Done!👏🏽

### Git commit issues
#### Commits not showing on the contribution calendar
This usually works for me. Even if I know I have the correct email associated I still run into this issue from time to time.  Try the bellow 👍🏽

``` 
$ git config user.email "my email address associated with my git repo"
```

## Windows

### Command line

#### Hyper.js setup
When setting up Hyper js you may run into a situation where Hyper js is not recognizing installed software. You check your node version and hyper.js spits out a "node is not a recognized...", in situations like these the below should help. Open up your hyper preferences and add this config.
```
module.exports = {

 config: {

  // default font size in pixels for all tabs

  fontSize: 12,



  // font family with optional fallbacks

  fontFamily: 'Menlo, "DejaVu Sans Mono", Consolas, "Lucida Console", monospace',



  // terminal cursor background color and opacity (hex, rgb, hsl, hsv, hwb or cmyk)

  cursorColor: 'rgba(248,28,229,0.8)',



  // `BEAM` for |, `UNDERLINE` for _, `BLOCK` for █

  cursorShape: 'BLOCK',



  // color of the text

  foregroundColor: '#fff',



  // terminal background color

  backgroundColor: '#000',



  // border color (window, tabs)

  borderColor: '#333',



  // custom css to embed in the main window

  css: '',



  // custom css to embed in the terminal window

  termCSS: '',



  // set to `true` (without backticks) if you're using a Linux setup that doesn't show native menus

  // default: `false` on Linux, `true` on Windows (ignored on macOS)

  showHamburgerMenu: '',



  // set to `false` if you want to hide the minimize, maximize and close buttons

  // additionally, set to `'left'` if you want them on the left, like in Ubuntu

  // default: `true` on windows and Linux (ignored on macOS)

  showWindowControls: '',



  // custom padding (css format, i.e.: `top right bottom left`)

  padding: '12px 14px',



  // the full list. if you're going to provide the full color palette,

  // including the 6 x 6 color cubes and the grayscale map, just provide

  // an array here instead of a color map object

  colors: {

   black: '#000000',

   red: '#ff0000',

   green: '#33ff00',

   yellow: '#ffff00',

   blue: '#0066ff',

   magenta: '#cc00ff',

   cyan: '#00ffff',

   white: '#d0d0d0',

   lightBlack: '#808080',

   lightRed: '#ff0000',

   lightGreen: '#33ff00',

   lightYellow: '#ffff00',

   lightBlue: '#0066ff',

   lightMagenta: '#cc00ff',

   lightCyan: '#00ffff',

   lightWhite: '#ffffff'

  },



  // the shell to run when spawning a new session (i.e. /usr/local/bin/fish)

  // if left empty, your system's login shell will be used by default

  // make sure to use a full path if the binary name doesn't work

  // (e.g `C:\\Windows\\System32\\bash.exe` instad of just `bash.exe`)

  // if you're using powershell, make sure to remove the `--login` below

  shell: 'C:\\Users\\abdja7r\\AppData\\Local\\Programs\\Git\\git-cmd.exe',



  // for setting shell arguments (i.e. for using interactive shellArgs: ['-i'])

  // by default ['--login'] will be used

  shellArgs: ['--command=usr/bin/bash.exe', '-l', '-i'],



  // for environment variables

  env: { TERM: 'cygwin'},



  // set to false for no bell

  bell: 'SOUND',



  // if true, selected text will automatically be copied to the clipboard

  copyOnSelect: false



  // if true, on right click selected text will be copied or pasted if no

  // selection is present (true by default on Windows)

  // quickEdit: true



  // URL to custom bell

  // bellSoundURL: 'http://example.com/bell.mp3',



  // for advanced config flags please refer to https://hyper.is/#cfg

 },



 // a list of plugins to fetch and install from npm

 // format: [@org/]project[#version]

 // examples:

 //  `hyperpower`

 //  `@company/project`

 //  `project#1.0.1`

 plugins: [],



 // in development, you can create a directory under

 // `~/.hyper_plugins/local/` and include it here

 // to load it and avoid it being `npm install`ed

 localPlugins: []

};

```
If after adding the above you run into an error it's most likely due to your git-cmd.exe path being wrong. Open your hyper preferences
go down to the line of code that contains SHELL 'C:\your git installation folder location \git-cmd.exe' and change it to the correct path of git-cmd.exe 

enjoy 🥳🎉
