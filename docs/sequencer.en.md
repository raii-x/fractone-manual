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

A song consists of 8 tracks and 32 patterns.
Patterns allow notes to be placed on the timeline, and tracks allow patterns to be placed on the timeline.
Basically, a single phrase of a song is used as a pattern, and multiple patterns are combined to create the composition of the song.
Tracks are created on Arrangement panel, and patterns are created on Edit panel.

## Operations on the desktop

On the desktop, VR operation and keyboard operation correspond as follows.

- Left stick: WASD
- Right stick: Arrow keys
- Left/right trigger: Left/right Shift
- Left/right grip: Left/right Ctrl or left/right Alt
- Rotate controller: Mouse up/down

## Operations

To select a panel, press the left grip shortly and then enter the left stick in the direction of the panel you wish to select.

### Operations common to all panels

- Left trigger short press: Play/Stop
- Left grip short press: Start panel selection
- Left stick: Move cursor
- Right stick ←→: Increase or decrease the value of an item
- Right stick ↑↓: Increase or decrease the value of an item significantly

### Operations common to both Arrangement and Edit panels

- Right grip: Delete value on cursor
- Right trigger long press: Get the value on the cursor
- Right trigger + Rotate right Controller: Increase or decrease the value according to the rotation
- Left grip + Right stick ←: Start/end range selection
- Left grip + Right stick ↓: Cut
- Left grip + Right stick →: Copy
- Left grip + Right stick ↑: Paste
- Left trigger + Rotate left controller: Move cursor according to rotation
- Left grip + Left trigger + Rotate left controller: Change zoom according to rotation

### Operations in Arrangement panel

- Left grip + Left stick ←: Set the start of the loop section
- Left grip + Left stick →: Set the end of the loop section

### Operations in Edit panel

- Right trigger short press: Insert note off

## Settings panel

Settings can be made for songs and patterns.

Next to the pencil icon, the values previously written in the Arrangement and Edit panels are displayed.

### Setting items

- BPM: Song tempo
- ZOOM (left side): Zoom in Arrangement panel
- PATTERN: Pattern to be edited
- INSTRUMENT: Instrument number used in the pattern
- ZOOM (right side): Zoom in Edit panel
- KEY: Transpose for note display only

## Arrangement panel

Patterns can be arranged on the timeline to create a song structure.

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
