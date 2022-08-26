## overview

pitch snap is a plugin that separates audio in real time into 20 sine partials and manipulates their pitch based on various parameters. it is inspired by the plugin retune by zplane, but it has a few additional features, like independent control of amplitude and frequency smoothing and an option to preserve the high end of the original sound. it also has around 100 times lower latency.

download the plugin from the "releases" page.

## warning

this plugin resets all parameters whenever it is loaded, even if the project it is loaded in is saved. this is a bug and i might look into fixing it if there's a lot of interest in the plugin. for now, you can bounce sounds to audio or automate any parameters you change to preserve their state. my recommendation is to bounce the wet signal so you can mix it in and maintain control of the dry signal.

## parameters

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

## credits

- [Pure Data](https://puredata.info/) by Miller Puckette and others
- [Camomile](https://github.com/pierreguillot/Camomile) by Pierre Guillot
