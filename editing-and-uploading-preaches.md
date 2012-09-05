Editing preaches
================

Introduction
------------

This guide will take you through the process of manipulating a preach recorded at a church event into something suitable for distributing for others to listen to.

The basic steps that we will follow are:

1. Import into editing software.
2. Trimming.
3. Normalisation.
4. Noise removal.
5. Compression.
6. Export.

After some practice this process can be completed in a few minutes.


Prerequisites
-------------

You will need some audio editing software. This guide will assume that you are using Audacity, if you do not have this installed, have a look for the 'Installing Audacity' guide in the PA team repo.

Import
------

Begin by starting a new project in Audacity: `File -> New`, and then immediately save this empty project: `File -> Save Project As…`. Use a suitable filename, ideally try to include the date, and the person talking on the track, so something like: `2012-09-17-Steven-Jones.aup` would be suitable.

With this clean, empty project you can import the recorded file, you can either drag and drop the file onto your Audacity project, or choose `File -> Import -> Audio` and find your file. After import your project should look something like this.

[INSERT SCREENSHOT]

Save your project and move onto the next section.

Trimming
--------

The imported audio track probably includes some audio before and after the main message that you want to remove. General guidelines for what to remove and what to keep are:

* Guideline 1
* Guideline 2

Start by finding the position you want the final export to start from by clicking on the track to set the playback start position and pressing the play button or the space-bar. You may wish to zoom in to the audio track to allow you to more accurately position the playback position, zoom controls are in the `view` menu.

When you've found the start position you want, use `Edit -> Select -> Track Start to Cursor` to select all the audio in the track up to that point, and then use `Edit -> Delete` to remove it.

Then do the same with the end point: Find the playback position at which the main message stops and then select the remaining audio with `Edit -> Select -> Cursor to Track End` and then delete that, again with `Edit -> Delete`.

If there's a region of audio in the middle of the recording that you need to remove you can drag a selection of audio and delete as before also.

After this stage you should have a recording that doesn't include any 'extras' but stills needs some tidy up before it's ready to be distributed.

Normalisation
-------------

To make it easier for people to listen to the track we're going to manipulate the audio. The main thing that we're going to do is normalise the audio so that the maximum gain is zero, this ensures that week to week the recording are all roughly the same volume when played back.

To normalise the audio choose `Effect -> Normalize…` which will bring up a dialog asking giving you a few options. The following is the default and is fine:

* Remove any DC offset (center on 0.0 vertically): _Enabled_
* Normalize maximum amplitude to: _Enabled and 0.0_

[INSERT SCREENSHOT]

Noise removal
-------------

Depending on the source the recording may contain a lot of background noise, that is competing with the person talking for the listeners attention.

Audacity has a nice plugin that will help you remove the noise, start by finding a section of the recording that _should_ otherwise be quiet, e.g. a long pause between the speaker saying one thing and another. Select this section of the recording so it's highlighted (click and drag) and play it over a few times to make sure it's just noise, avoid using sections where the speaker can be heard making 'background' noises, e.g. having a sip of water or changing pages in notes.

Once you've selected the section of pure noise, choose `Effect -> Noise Removal…` and press the step 1 button: `Get Noise Profile`. Audacity will sample the section you've selected to work out what you think is noise.

Now, select the entire recording (`Edit -> Select -> All`) and then choose the effect again: `Effect -> Noise Removal…` and this time use the lower portion of the dialog to apply the noise removal. This might require some trial and error with settings to remove the noise without distorting the audio that you actually want to keep, but a good baseline to start from would be:

* Noise reduction (dB): _15_
* Sensitivity (dB): _2.56_
* Frequency smoothing (Hz): _400_
* Attack/decay time (secs): _0.15_

You can use the preview button to hear what the first few seconds of the recording would sound like with you current settings applied before you've applied them to your entire recording, which can take a little while be computed and applied.


Compression
-----------

Next we'll run the audio through a compressor, this will will reduce the recordings 'dynamic range' which basically means that we're reducing the difference between the loudest and quietest parts. This will help people listen to the recording when there's lots of background noise, when they're listening in the car, for example.

To run the compressor choose `Effect -> Compressor…` and then use the following settings:

* Threshold: _-30 dB_
* Noise Floor: _-55 dB_
* Ratio: _3:1_
* Attack Time: _0.2 secs_
* Decay Time: _1.0 secs_
* Make-up gain to 0dB after compressing: _Enabled_
* Compress based on Peaks: _Disabled_

[INSERT SCREENSHOT]

Export
------

Finally we must export the file as an MP3 suitable for distributing, do this by choosing `File -> Export…`, choose a suitable filename, and in the 'Format' drop-down choose: _MP3 Files_, if you don't have this option, have a read through the PA Team Audacity installation guide.

Then press the `Options` button to configure the type of MP3 file that is going to be produced, ensure the following options are selected:

* Bit Rate Mode: _Constant_
* Quality: _80 kbps_
* Channel Mode: _Joint Stereo_

Press `Save` and your recording will be exported ready for distribution.