# Trubadur

Trubadur is an Open Source and FREE software for editing your lyrics and guitar chords/tabs.

## License

[MIT license](https://github.com/trubadur-app/trubadur-source/blob/master/LICENSE.md)


## Installation

1. Make sure you have [Java](https://www.java.com/en/download/) installed and updated to the latest version
2. Find the [latest version](https://github.com/trubadur-app/trubadur/releases/latest) of the Trubadur application. Download the file called `trubadur-1.*.*.*.jar`, for instance `trubadur-1.0.0.jar` but with the latest version instead of version 1.0.0. This is found under "Assets".
4. Create a directory somewhere on your computer (for instance in your Applications directory) and name it "Trubadur"
5. Place the JAR-file you downloaded in this newly created directory
6. You can now run the JAR-file like a normal application by double-clicking


**Note!** Once you have run the application for the first time there is a directory created next to the JAR-file called `data`. This is where all your application data is stored. Make sure to regurarly backup this directory so that you always can restore the application data if you ever loose it.

![Data folder](https://github.com/trubadur-app/trubadur/blob/master/images/file3.png)


## How it works

The Trubadur application is a JAR-file that can be run to open the application on a desktop computer. When it opens for the first time, a `data` directory is created next to the application JAR-file.

This data directory contains all the data you input to the application, such as the songs, playlists and labels. This means that your application data is stored on your computer where you are running the application.


### Browser view

In addition to the desktop application (the JAR-file), you can also view your application data in a web browser, for instance Google Chrome, Firefox or Safari. However, when you use the application in the browser you will not be able to make any changes to the data, only view your content. Changes are always made through the dekstop application (the JAR-file).

To view the application in the browser with your content you need to locate the `trubadur-read-only-data-copy.json` file, which is a read-only copy of your application data, that is stored in the `data` directory, i.e. `data/trubadur-read-only-data-copy.json`.

This file is generated automatically after each time you close the desktop application, and contains a duplication and read-only version of your application data. It is safe to delete this file or move it, since your application data is stored in the subdirectories of the `data` directory, e.g. `data/song`, `data/playlist`, and since this file is created again when you close the application next time.

You can now enter the following [web page](https://storage.googleapis.com/trubadur-app-read-only/index.html). When asked for a data-file, you simply select the `trubadur-read-only-data-copy.json` file from your computer. This file will be locally processed in your browser, and you can now view your application content in your browser.


### Mobile support

If you want to view your application content in your browser on a mobile or tablet device, you can use the "Browser view" which is explained above and open the [url](https://storage.googleapis.com/trubadur-app-read-only/index.html) on your mobile/tablet device. This means, however, that you need to transfer your `trubadur-read-only-data-copy.json` file to your other device in order to load it in that device's browser. This can be done, for instance, by putting the `trubadur-read-only-data-copy.json` file in an Online Storage, such as Dropbox or Google Drive, and synchronize that storage to your other device.

In the settings view of the Trubadur dekstop application you can select a different path for the `trubadur-read-only-data-copy.json` file, other than the default path `data/trubadur-read-only-data-copy.json`, if you want the read-only data file to be saved elsewhere on your computer everytime the Trubadur application is closed. The settings view can be opened by pressing the "cog" icon in your Trubadur desktop application.

Under "File path for read-only data copy" you can then select a different path for your `trubadur-read-only-data-copy.json` file.


## Report a bug

Found a bug? You can report it to the developers of the Trubadur application by going to [this page](https://github.com/trubadur-app/trubadur/issues) and creating a new issue. Please check first if the bug has already been reported before. If it hasn't been reported before, create a new issue and add the label **bug**. Describe the bug you found in detail with:

1. What you did in the application that led to the bug
2. What you experienced (i.e. describe the bug itself)
3. What you expected to happen instead.


## Suggest a feature

Do you want to suggest a new feature to the developers of the Trubadur application? We happily take suggestions for new features. However, they can only be developed if any of the developers have the time for it and if the developers agree that the feature is needed. To suggest a new feature, you can do so by going to [this page](https://github.com/trubadur-app/trubadur/issues) and creating a new issue. Please add the label **enhancement**, and describe the feature you are suggesting. Please make sure that the feature has not been suggested already, before you create a new issue.


## Missing chord

Is there a chord missing in the application? This is apparent by the chord not being recognized by the application. Example:

You can report it by going to [this page](https://github.com/trubadur-app/trubadur/issues) and creating a new issue. Please check before if the missing chord has already been reported. If you create a new issue, add the label **missing chord** to the new issue. You can assist with adding the chord to the application by filling out the following template and adding it to the issue:

```
Chord: 

Guitar instructions:
A: [0,0,0,0,0,0]
A#:	...
B:
C:
C#:
D:
D#:
E:
F:
F#
G:
G#:
```

You need to define guitar instructions for each of the 12 semitones so that transposing works for the chord. The [0,0,0,0,0,0] part should represent how to play the chord on the guitar for the given semitone, where the first number is for the low E string, the second number is for the A string etc. The number represents the fret number on the guitar. If you put -1 it means that the string should not be played.


Here is an example if we were to suggest the chord "minor" (e.g. Am, Bm, Cm ...):

```
Chord: Minor

Guitar instructions:
Am: [-1,0,2,2,1,0]
A#m: [6,8,8,7,6,6]
Bm: [7,9,9,7,7,7]
Cm: [8,10,10,8,8,8]
C#m: [-1,4,6,6,5,4]
Dm: [-1,-1,0,2,3,1]
D#m: [-1,6,8,8,7,6]
Em: [0,2,2,0,0,0]
Fm: [1,3,3,1,1,1]
F#m: [2,4,4,2,2,2]
Gm: [3,5,5,3,3,3]
G#m: [4,6,6,4,4,4]
```

If you know how to work with Github and JSON, you can make changes to [this file](https://github.com/trubadur-app/trubadur-source/blob/master/src/frontend/javascripts/song-text-parse/music-theory/music-theory-data.js) directly and submit a merge request to the `trubadur-source` repository.


## Changelog

The changelog, explaining what each new version contains, can be found [here](https://github.com/trubadur-app/trubadur-source/blob/master/CHANGELOG.md).


## Code

The code for the Trubadur software can be found [here](https://github.com/trubadur-app/trubadur-source).

