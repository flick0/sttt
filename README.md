# A Solution to your Terminal Transition Tribulation

ever wanted to add cool transitions to your terminals? no? well let me present to you the solution to a [tribulation](https://letmegooglethat.com/?q=tribulation) you didnt even know you were in

## Features + Roadmap

+ [x] cubic bezier easing
+ [x] reactive to terminal size
+ [x] loop/reverse transitions
+ [x] set duration for transition
+ [x] transitions
+ [ ] more transitions
+ [ ] actual cli

## Installing

the entire thing is just one file so you can curl/wget it and add to path

using curl:
```sh
sudo curl -L https://raw.githubusercontent.com/flick0/sttt/main/sttt -o /usr/local/bin/sttt
sudo chmod a+rx /usr/local/bin/sttt
```

or with wget:
```sh
sudo wget https://raw.githubusercontent.com/flick0/sttt/main/sttt -o /usr/local/bin/sttt
sudo chmod a+rx /usr/local/bin/sttt
```

## Transitions

+ ScanLine
  > scanline with reverse set to `true`, `width` as `2`, `scale_width` as `1.1`, and `scale_ratio` as `0.5` meaning the width is gonna scale by `1.1` with the maximum width at `0.5`
  ![scanline](https://github.com/flick0/sttt/assets/77581181/d501dc17-7b23-4704-8404-1f44ab753ee8)

+ Grow
  > ![grow](https://github.com/flick0/sttt/assets/77581181/b67bf986-99c7-4d72-9fa9-8be4d02ffa71)
  
+ Shrink
  > shrink with center position set to `[0.9,0.5]` meaning its at 90% width and 50% height
  ![shrink](https://github.com/flick0/sttt/assets/77581181/94600752-6ee0-48eb-855a-62a0c38a6093)

+ GrowExit
  > growexit with center of first circle set as `[0.3,0.3]` and `[0.7,0.7]` for the second circle
  ![growexit](https://github.com/flick0/sttt/assets/77581181/804732b0-63c8-470e-9581-631804aaeb77)


+ ShrinkExit
  > shrinkexit with `second_start` set to `0.9` meaning 90% of duration is used for first circle and the rest 10% for the second circle
  ![shrinkexit](https://github.com/flick0/sttt/assets/77581181/e452a474-3d1e-473d-b3f4-c628be14feee)

## its also reactive to terminal size changes!
  > GrowExit transition with loop and reverse enabled
    ![resize](https://github.com/flick0/sttt/assets/77581181/7d52b7d1-5968-46a7-94a2-d9e44e25bd35)



## Why?

this was supposed to be a tiny little script that does only one linear transition for a [rice im working on](https://github.com/flick0/dotfiles) which ended up taking more of my time than i intended, the idea was partly inspired by [unimatrix](https://github.com/will8211/unimatrix)(the `-w` flag to be precise, which suggests you to put it in .bashrc to run when terminal launches)

## [SWWW](https://github.com/Horus645/swww)?

if the name isnt clear enough( *"swww"* and *"sttt"* ) most of the inspiration comes from swww, the way transitions are made is also pretty similar 
to how swww does it, if somehow you havent heard of swww before, [do go check it out](https://github.com/Horus645/swww), its a wayland wallpaper daemon with fancy transitions

## Thanks!

+ to [bezier-easing](https://github.com/gre/bezier-easing) which i directly translated to python because apparently there are no good cubic bezier easing libs i could find for python
