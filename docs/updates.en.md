# Updates

* 2024/6/24
    * Added track mute and solo functions to the sequencer
    * Changed so that note-off is performed as it was before the 2024/6/23 update, when note-off is at the following positions
        * The end position of the previously played pattern when the next pattern is played
        * The end position of the loop when returning from the loop end position to the loop start position
* 2024/6/23
    * The playback position is now synchronized with the person who joined after the sequencer playback
    * For LFOs with Trigger turned off, the phase is reset when the sequencer is played from the beginning, and the phase is set so that when the sequencer is played from the middle, the phase is the same as when it was played from the beginning
    * Changed so that when the next pattern is played, the part of the pattern after the end position of the previously played pattern is not played
    * Changed so that notes after the end of the loop are not played when returning from the loop end position to the loop start position
    * Fixed a problem where the cursor was not visible when the cursor was moved to the end of the sequencer
    * Fixed an error when pasting in the sequencer when the position of the pasted content exceeds the end position
* 2024/6/16
    * Added auto save function
    * Fixed a problem that the world menu had an unclickable area when on the desktop
* 2024/6/13
    * Increased the number of available Instruments to 16
    * Shortened the length of saved data when the waveform has not been changed from the preset
* 2024/1/7
    * Added NOISE to the WARP TYPE in WAVEFORM
* 2023/12/31
    * Added the manual in the world
* 2023/12/4
    * Fixed a problem that the world menu was not grabbable
    * Fixed that synthesizer buttons were hard to press
    * Fixed the Clear button under the pen not moving from its initial position
* 2023/11/28
    * Fixed that the sequencer could not be exited by pressing the menu button
    * Allow Alt to be used instead of Ctrl for sequencer keyboard operations
* 2023/7/24
    * Fixed a problem where switching or loading Instrument while holding a modulation plug in your hand would leave you holding an invisible plug
    * Changed so that when switching Instrument, it does not note off the Instrument sound before switching
* 2023/7/16
    * Fixed a problem with small avatars not being able to grab the world menu
* 2023/7/14
    * Released the world
