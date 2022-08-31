## overview

pitch snap is a plugin that separates audio in real time into 20 sine partials and manipulates their pitch based on various parameters. it is inspired by the plugin retune by zplane, but it has a few additional features, like independent control of amplitude and frequency smoothing and an option to preserve the high end of the original sound. it also has around 100 times lower latency.

download the plugin from the "releases" page.

## parameters

- the column on the right side allows for auditioning notes and chords before they are selected in the grid. it can be reset with the button at the top.
- the grid allows each note in a scale to be shifted to a different note. for example, all instances of 'c#' can be shifted to 'e'. notes are ordered from c (bottom) to b (top), although the base note can be shifted by semitones with the "pitch" control.
- "freq smooth" limits how quickly partials can change in frequency. at zero, partials can jump between frequencies instantly, which creates satisfying textures on certain sounds. higher levels create pitch glides. 
- "amp smooth" limits how quickly partials can change in volume. it sounds similar to the attack and release knobs on a vocoder.
- "pitch correct" scales the amount of pitch variation within each semitone from 0 (all the pitch variation of the original sound) to 1 (no pitch variation)
- "pitch" controls pitch of the wet signal in semitones. to adjust it in small increments, hold the shift key before clicking and dragging.
- "high split" when enabled allows the high frequencies of the dry signal to pass through and rolls off the high frequencies of the wet signal. this is useful because the wet signal is bandlimited above the highest frequency of the first 20 partials.
- "mix" allows the dry signal to be mixed in.

## installation

to install this plugin, extract it into your vst3 folder.
- on windows the folder is normally c:\program files\common files\vst3
- on mac the folder is normally library/audio/plug-ins/vst3

## changing source files

the architecture of this plugin allows users to edit source files on the fly and apply changes to the plugin simply by reloading it. the camomile wiki and pure data manual are good starting points if you're looking to make changes or even make your own pure data plugins. 

## credits

- [pure data](https://puredata.info/) by miller puckette and others
- [camomile](https://github.com/pierreguillot/Camomile) by pierre guillot
