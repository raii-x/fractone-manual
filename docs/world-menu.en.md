# World menu

The World menu allows you to make settings related to worlds, synthesizers, and sequencers.

* In VR, hold the right controller stick pushed up to display it.
  Alternatively, grab the back of your head and it will appear at the position of your hand.
* On the desktop, press the Q key to display it.

## WORLD tab

Configures settings related to the world.

* QvPen: Toggles the visibility of QvPen (global).
* Floor Collider: Sets the height of the floor collider (local).

## CONTROL tab

* Instrument: Toggles between instruments to be edited in the synthesizer (global).
* Sequence: Play/stop the sequencer (global).
* MIDI CH to Inst.: When turned on, channels 1-16 of the external MIDI keyboard input are mapped to Instruments 0-F (local).

## FILE tab

You can save and load the data you have created.
Data is saved using VRChat's Persistence and will be retained even after leaving the world.
Up to 100 KB of compressed size and up to 100 files can be saved.

### Overall size display

The overall size of the saved data after compression is displayed in the upper right of the panel.
Because it takes time to obtain the actual size, immediately after saving and similar operations an overestimated size is shown in a faint color,
and once the retrieval is complete the actual size is displayed at the original intensity.

### Data type selection

* Song: Saves all Instrument and sequencer edit data together.
* Instrument: Saves the currently edited Instrument.
* WAV: Saves waveform data.
* Sequence: Saves the sequencer edit data.

### File selection

A list of saved files is displayed for the selected data type.
The file name, modification date and time, and the uncompressed file size are displayed in the file line.
"New File..." is selected, you can save the data in a new file.

### Operation buttons

* Load: Loads the selected file.
  A dialog box is displayed and the "Load" button is pressed to complete loading.
* Save: Saves the data in the selected file.
  A dialog box appears. For a new file, enter a file name in the "File Name" field and press the "Save" button to complete saving.
  If you are saving to an existing file, click the "Save" button to overwrite the file.
* Rename: Renames the selected file.
  A dialog box will appear. Enter a new file name in the "File Name" field and press the "Rename" button to rename the file.
* Delete: Deletes the selected file.
  A dialog box appears, and then press the "Delete" button to complete the deletion.

If an error occurs during saving, an error message will appear in the dialog.
If the message "No file slots available." is displayed, the maximum limit of 100 files that can be saved has been reached and the file must be deleted in order to save.
"Total size exceeds maximum limit of 100 KB." is displayed, the total size of the data exceeds 100 KB when saving, and you must delete the data to free up space to save.

### Auto save

Turning on the AutoSave button in the lower right of the tab enables auto save.

* Data is saved automatically every 5 minutes to a file named [AutoSave].
* It is saved only when the data has changed since the previous auto save.
* Up to 3 auto save files are created, and when 3 files exist the oldest one is overwritten.
  If you want to keep it, rename it.

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

## UTILITY tab

For Instrument and Pattern, you can either swap or copy between the two items.

Select whether to target Instrument or Pattern on the tabs at the top.
Specify the two numbers to be targeted in "From" and "To".

Press the Swap button to swap the items specified in "From" and "To".
In this case, in the case of Instrument, the Instrument number specified in Pattern is also swapped, and in the case of Pattern, the Pattern number specified in Track is also swapped.
When the Copy button is pressed, the item specified in "From" is copied to "To".
