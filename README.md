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
- All of my Conky are using Roboto, Noto-Sans, and M+ fonts.
- Some of these are designed for 1366x768 screen resolution.
- The transparency is using *fake transparency* method, because I can take an advantage on Openbox (my favourite window manager).
The transparancy would still work even if I didn't install any external compositor like compton.
Maybe couldn't work if your DE is not respecting fake transparency.
Switch to *true transparency* / *ARGB transparency* instead.
Check the *issues* tab. 
- Again, Inspect the code before use.
- I will add more themes later.
- I'm not good at creating name for the themes.
I just randomly pick name for them.
- Some of Conky are unstickied. It means, the conky would be visible on one workspace only.
I do it on large size Conky to make it not distracting on my working workspace.
If You want to make it available on every workspace, change
`own_window_type = 'normal'` to `own_window_type = 'desktop'`.
- Different Distro probably has different font version & font config.
This affect the font kerning and spacing. This make the image and the text misaligned.
Maybe You can try to change the images coordinate or change the text placement using `offset` if You find the image & text misaligned.
- Probably couldn't work out of the box :stuck_out_tongue_winking_eye:
- You should listen to Dream Theater, Metallica, Nirvana, Led Zeppelin, NOFX, Alice in Chain, Linkin Park,
Pearl Jam, Slipknot, System of a Down, Soundgarden, Dragonforce, Radiohead, Red Hot Chilli Peppers (before John Frusciante left),
Muse (before *The 2nd Law* album), Greenday (before they join MTV), and Superman is Dead (until *Black Market Love* album).
- Don't listen to Nickelback.

## Preview

## Sidekick
![sidekick](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-sidekick.jpg) <br />

## Flea
![flea](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-flea.jpg) <br />

## Sidepanes
![sidepanes](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-sidepanes.jpg) <br />

## Syclo
![syclo](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-syclo.jpg) <br />

## Novoselic
![novoselic](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-novoselic.jpg) <br />

## Cliff
![cliff](https://raw.githubusercontent.com/addy-dclxvi/conky-theme-collections/master/preview-cliff.jpg) <br />

## Installations
Simply just clone this repo to your Conky configurations folder <br />
`git clone https://github.com/addy-dclxvi/conky-theme-collections ~/.config/conky --depth 1`

Then load it using `conky -c` command. For example <br />
`conky -c ~/.config/conky/sidepanes/sidepanes.conkyrc` <br />
Add it to your startup to make your life easier :wink:

## Credits
- Quotes are taken from quotationspage.com using script I got from
  [here](https://gist.github.com/SahilC/2767b6681539d96c4f37)
- Weather script is taken from Anachron
- Some icons are extracted from Min icons pack

