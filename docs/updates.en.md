# Updates

* 2025-07-15
    * Fixed a problem where synchronized notes would remain sounding after note-off
* 2025-07-15
    * Added save/load functionality using Persistence
    * Improved synchronization stability
    * Improved timing accuracy of world keyboard and MIDI input synchronization
* 2024-09-19
    * Fixed a problem where the input threshold for grips in the sequencer was at a shallow position when using the Index controllers
    * Fixed a problem where plugs could no longer be dropped with the Quest and Index controllers
* 2024-07-10
    * Added behavior in the sequencer where a note with an empty pitch and velocity only changes the velocity of a note that is already sounding
    * Added effect commands to the sequencer (Pitch slide down, Pitch slide up, Glide)
* 2024-07-06
    * Increased the number of available tracks to 16 and the number of patterns to 64
    * Added manual channel assignment function to the sequencer
    * Fixed the problem that the Instrument number displayed when changing the edit pattern in the sequencer was a decimal number
* 2024-06-29
    * Added UTILITY tab to the world menu
* 2024-06-25
    * Added a function to edit the pattern on the cursor in the Arrange panel of the sequencer
    * Changed to be able to zoom to 1/96 in the Arrange panel of the sequencer
* 2024-06-24
    * Added track mute and solo functions to the sequencer
    * Changed so that note-off is performed as it was before the 2024-06-23 update, when note-off is at the following positions
        * The end position of the previously played pattern when the next pattern is played
        * The end position of the loop when returning from the loop end position to the loop start position
* 2024-06-23
    * The playback position is now synchronized with the person who joined after the sequencer playback
    * For LFOs with Trigger turned off, the phase is reset when the sequencer is played from the beginning, and the phase is set so that when the sequencer is played from the middle, the phase is the same as when it was played from the beginning
    * Changed so that when the next pattern is played, the part of the pattern after the end position of the previously played pattern is not played
    * Changed so that notes after the end of the loop are not played when returning from the loop end position to the loop start position
    * Fixed a problem where the cursor was not visible when the cursor was moved to the end of the sequencer
    * Fixed an error when pasting in the sequencer when the position of the pasted content exceeds the end position
* 2024-06-16
    * Added auto save function
    * Fixed a problem that the world menu had an unclickable area when on the desktop
* 2024-06-13
    * Increased the number of available Instruments to 16
    * Shortened the length of saved data when the waveform has not been changed from the preset
* 2024-01-07
    * Added NOISE to the WARP TYPE in WAVEFORM
* 2023-12-31
    * Added the manual in the world
* 2023-12-04
    * Fixed a problem that the world menu was not grabbable
    * Fixed that synthesizer buttons were hard to press
    * Fixed the Clear button under the pen not moving from its initial position
* 2023-11-28
    * Fixed that the sequencer could not be exited by pressing the menu button
    * Allow Alt to be used instead of Ctrl for sequencer keyboard operations
* 2023-07-24
    * Fixed a problem where switching or loading Instrument while holding a modulation plug in your hand would leave you holding an invisible plug
    * Changed so that when switching Instrument, it does not note off the Instrument sound before switching
* 2023-07-16
    * Fixed a problem with small avatars not being able to grab the world menu
* 2023-07-14
    * Released the world
