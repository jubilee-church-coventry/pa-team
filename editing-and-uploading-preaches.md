Editing preaches
================

Introduction
------------

This guide will take you through the process of manipulating a preach recorded at a church event into something suitable for distributing for others to listen to.

The basic steps that we will follow are:

1. Import into editing software.
2. Trimming.
3. Normalisation and compression.
4. Export.

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

Start by finding the position you want the final export to start from by clicking on the track to set the playback start position and pressing the play button or the space-bar. You may wish to zoom in to the audio track to allow you to more acurately position the playback position, zoom controls are in the `view` menu.

When you've found the start position you want, use `Edit -> Select -> Track Start to Cursor` to select all the audio in the track up to that point, and then use `Edit -> Delete` to remove it.

Then do the same with the end point: Find the playback position at which the main message stops and then select the remaining audio with `Edit -> Select -> Cursor to Track End` and then delete that, again with `Edit -> Delete`.

If there's a region of audio in the middle of the recording that you need to remove you can drag a selection of audio and delete as before also.

After this stage you should have a recording that doesn't include any 'extras' but stills needs some tidy up before it's ready to be distributed.

Normalisation and compression
-----------------------------

To make it easier for people to listen to the track we're going to manipulate the audio. The main thing that we're going to do is normalise the audio so that the maximum gain is zero, this ensures that week to week the recording are all roughtly the same volume when played back.

To normalise the audio choose `Effect -> Normalize…` which will bring up a dialog asking giving you a few options. The following is the default and is fine:

[INSERT SCREENSHOT]

Next we'll run the audio through a compressor, this will...

Export
------