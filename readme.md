Dataset created for evaluating the performance of Dechord (https://github.com/lucmans/dechord).

# Technical details
The files were recorded by directly plugging a guitar with active pick-ups into a Behringer UMC404HD audio interface. Audacity was used to capture the audio and write it to a file. No software amplification was applied.

All files are in RIFF WAVE format, using float32 samples at a sample rate of 192000 Hz and a single channel (mono).

Even though the pre-amp gain was maximized (without clipping) in the audio interface, the samples are very quiet (well within [-0.1, 0.1] instead of [-1.0, 1.0]). We opted not to perform software amplification on the files to preserve the original recording. In general, software amplification or other signal processing should be applied by the program using these files and taken into consideration when evaluating performance.


# Data subsets
The data set is split into 2 subsets, scales and intervals.

## `scales`
The scales subset is created to measure monophonic performance. All scales are played in C at 120 BPM (2 notes per second). Each file contains the full vertical scale (www.all-guitar-chords.com/scales) from different starting notes (17 to 18 notes).

The filenames are build up as `<key>_<starting note>_<bpm>.wav`, where `<bpm>` is the integer BPM, `<key>` is the key in which the scale is played and `<starting note>` first note which indicates which vertical position is played.

The low speed of 120 BPM helps against transient errors, as the transients are relatively much shorter compared to the note length.

## `intervals_2`
The intervals 2 subset is created to measure polyphonic performance. Every file consists of a two note interval separated by 1 to 11 semitones.

The filenames are build up as `<starting note>_<n>.wav`, where `<starting note>` is the lower of the two notes seperated by `n` semitones.
