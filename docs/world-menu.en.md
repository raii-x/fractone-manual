# World menu

The World menu allows you to make settings related to worlds, synthesizers, and sequencers.

* In VR, grab the back of your head and it will appear at the position of your hand.
* On the desktop, press the Q key to toggle the display.

## WORLD tab

Configures settings related to the world.

* QvPen: Toggles the visibility of QvPen (global).
* Floor Collider: Sets the height of the floor collider (local).

## CONTROL tab

* Instrument: Toggles between instruments to be edited in the synthesizer (global).
* Sequence: Play/stop the sequencer (global).

## IMPORT tab

Data can be loaded by pasting the data output on the EXPORT tab into the text box.
After pasting the data into the text box, press the Load button to complete loading.

In case of an error, error message will be displayed in the dialog.

## EXPORT tab

Pressing the button corresponding to each data will output the data as text in a text box.

* Song: Outputs all Instrument and sequencer edit data together.
* Instrument: Outputs the currently edited Instrument.
* WAV1, WAV2: Outputs the waveform data.
* Sequence: Outputs the sequencer edit data.

When Auto Save is enabled, Song save data is automatically output to the VRChat log every 2 minutes.
The log will be saved in a file named starting with `output_log_` in `C:\Users\%USERNAME%\AppData\LocalLow\VRChat\VRChat`.

## UTILITY tab

For Instrument and Pattern, you can either swap or copy between the two items.

Select whether to target Instrument or Pattern on the tabs at the top.
Specify the two numbers to be targeted in "From" and "To".

Press the Swap button to swap the items specified in "From" and "To".
In this case, in the case of Instrument, the Instrument number specified in Pattern is also swapped, and in the case of Pattern, the Pattern number specified in Track is also swapped.
When the Copy button is pressed, the item specified in "From" is copied to "To".
