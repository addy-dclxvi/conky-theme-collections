## Introduction
Just my homebrew Conky collections

## Getting Started & Notes
- Need Conky 1.10
- To make sure it works, use conky with all build options enabled.
  Use `conky-all` package if You're on Debian.
- Music widget is for `mpd`.
- Album art script is not very elegant.
  It just crawls the folder where You play the music using `mpc`,
  then print any image it found in that folder to Conky.
  I just want to make it simple.
- Weather script needs `wget`.
- Inspect and edit all script in the subfolders before use.
- Script execution denied? Do `chmod +x` to the denied script.
- You can get OpenWeather API code after register to  http://openweathermap.org
- You can get City ID from http://openweathermap.org/find
- All of my Conky are using Roboto & Noto-Sans fonts.
- Some of these are designed for 1366x768 screen resolution.
- The transparency is using *fake transparency* method.
  Maybe couldn't work if your DE is not respecting fake transparency.
  Switch to *true transparency* / *ARGB transparency* instead.
  Check the *issues* tab. 
- Again, Inspect the code before use.
- I will add more themes later.
- I'm not good at creating name for the themes.
  I just randomly pick name for them.
- Probably couldn't work out of the box :stuck_out_tongue_winking_eye:

## Preview

## Sidekick
![sidekick](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-sidekick.jpg) <br />

## Flea
![flea](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-flea.jpg) <br />

## Sidepanes
![sidepanes](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-sidepanes.jpg) <br />

## Installations
Simply just clone this repo to your Conky configurations folder <br />
`git clone https://github.com/addy-dclxvi/Conky-Theme-Collections ~/.config/conky --depth 1`

Then load it using `conky -c` command. For example <br />
`conky -c ~/.config/conky/sidepanes/sidepanes.conkyrc` <br />
Add it to your startup to make your life easier :wink:

## Credits
- Quotes are taken from quotationspage.com using script I got from
  [here](https://gist.github.com/SahilC/2767b6681539d96c4f37)
- Weather script is taken from Anachron
- Some icons are extracted from Min icons pack

