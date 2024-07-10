# Sequencer

The sequencer screen on the left side of the synthesizer is where you can create a song.

Fractone uses a tracker style sequencer.
The sequencer does not use a laser pointer, but rather a controller to move the cursor and write values.

When the sequencer is interacted with, both controller inputs are sent to the sequencer and normal movement operations are disabled.
Pressing the menu button will release the sequencer input and allow normal movement.

![Sequencer](images/sequencer.png)

The sequencer has several panels: Settings panel on the top, Arrangement panel on the left, and Edit panel on the right.
Of these, controller inputs are made to the currently selected panel.
The currently selected panel is indicated by a red frame.

A song consists of 16 tracks and 64 patterns.
Patterns allow notes to be placed on the timeline, and tracks allow patterns to be placed on the timeline.
Basically, a single phrase of a song is used as a pattern, and multiple patterns are combined to create the composition of the song.
Tracks are created on Arrangement panel, and patterns are created on Edit panel.

## Operations on the desktop

On the desktop, VR operation and keyboard operation correspond as follows.

* Left stick: WASD
* Right stick: Arrow keys
* Left/right trigger: Left/right Shift
* Left/right grip: Left/right Ctrl or left/right Alt
* Rotate controller: Mouse up/down

## Operations

To select a panel, press the left grip shortly and then enter the left stick in the direction of the panel you wish to select.

### Operations common to all panels

* Left trigger short press: Play/Stop
* Left grip short press: Start panel selection
* Left stick: Move cursor
* Right stick ←→: Increase or decrease the value of an item
* Right stick ↑↓: Increase or decrease the value of an item significantly

### Operations common to both Arrangement and Edit panels

* Right grip: Delete value on cursor
* Right trigger long press: Get the value on the cursor
* Right trigger + Rotate right Controller: Increase or decrease the value according to the rotation
* Left grip + Right stick ←: Start/end range selection
* Left grip + Right stick ↓: Cut
* Left grip + Right stick →: Copy
* Left grip + Right stick ↑: Paste
* Left trigger + Rotate left controller: Move cursor according to rotation
* Left grip + Left trigger + Rotate left controller: Change zoom according to rotation

### Operations in Arrangement panel

* Left grip + Left stick ←: Set the start of the loop section
* Left grip + Left stick →: Set the end of the loop section
* Left grip + Left stick ↓: Mute track
* Left grip + Left stick ↑: Solo track
* Right trigger short press: Select the pattern on or above the cursor and go to Edit panel

### Operations in Edit panel

* Right trigger short press: Insert note off or effect command

## Settings panel

Settings can be made for songs and patterns.

Next to the pencil icon, the values previously written in the Arrangement and Edit panels are displayed.

### Setting items

* BPM: Song tempo
* ZOOM (left side): Zoom in Arrangement panel
* PATTERN: Pattern to be edited
* INSTRUMENT: Instrument number used in the pattern
* ZOOM (right side): Zoom in Edit panel
* KEY: Transpose for note display only
* CHANNEL: Whether channel assignment is done automatically or manually (see below for details)

## Arrangement panel

Patterns can be arranged on the timeline to create a song structure.

At the top, the track number is displayed if the track is not muted, or "M" if the track is muted.
Patterns are displayed as hexadecimal numbers.

Songs are played and stopped at the cursor position in Arrangement panel.
The loop section when playing a song is also specified in Arrangement panel.

## Edit panel

The notes can be placed on the timeline to create a pattern.

The instrument used in the performance will be the one specified on the settings panel.

The pattern consists of 8 columns, and notes can be placed in each column.

There are two types of notes: note-ons, which sound a note, and note-offs, which stop sounding a note.
A note sounded in note-on will continue to sound until a note-off or another note-on arrives in the same column.

Note-ons consist of pitch and velocity, with pitch displayed as a note name and octave, such as "C-4," and velocity displayed as a number from 00 to 7F in hexadecimal.
Note-offs are displayed as "off".
If you omit the velocity of a note, the velocity will be the same as if you had specified 7F.
A note with an empty pitch and velocity only changes the velocity of the already sounding note.

### Effects Commands

You can insert an effect command by briefly pressing the right trigger while the cursor is on velocity.
Effect commands are commands to apply special effects to notes.
Effect commands have an effect type and an effect amount, where the effect type is a single letter of the alphabet and the effect amount is a hexadecimal number from 0 to F.

#### Effect Type

* D (pitch slide Down): lowers the pitch of the note
* U (pitch slide Up): Raises the pitch of the note
* G (Glide): Smoothly changes the pitch of the note already sounded to the pitch of the note for which this effect is specified

#### Effect amount

The effect amount represents the speed of the pitch change.

* 0: Stop pitch change for pitch up and pitch down, change the pitch to the note immediately for glide
* 1: 1 semitone/quarter note
* 2: 1.5 semitones/quarter note
* 3: 2 semitones/quarter note
* 4: 3 semitones/quarter note
* 5: 4 semitones/quarter note
* 6: 6 semitones/quarter note
* 7: 8 semitones/quarter note
* 8: 12 semitones/quarter note
* 9: 16 semitones/quarter note
* A: 24 semitones/quarter note
* B: 32 semitones/quarter note
* C: 48 semitones/quarter note
* D: 64 semitones/quarter note
* E: 96 semitones/quarter note
* F: 128 semitones/quarter note

## Channel Assignment

In Fractone, the audio source to which the sound to be played is assigned is called a channel.
Fractone has 16 channels, so up to 16 notes can be sounded simultaneously.

When a note is played on the keyboard or when CHANNEL is set to AUTO on the sequencer's Settings panel, the note to be played is automatically assigned to an available channel.
However, the effects used for tones can affect the sound even after the sound has finished sounding, and if tones with different effects are assigned to the same channel after sounding, the sound may have undesired effects.
In such a case, you can specify the channel to be manually assigned to the sound by specifying CHANNEL to MANUAL in the Settings panel.

When using manual channel assignment, the channel number assigned to notes played within a pattern placed on a track is the remainder of (track number + column number in the pattern) divided by 16.
For example, a pattern placed on track 1 would be assigned to channels 1, 2, 3, ... from the left column, and a pattern placed on track 15 (F on the sequencer display) would be assigned to channels 15, 0, 1, ... from the left column.
