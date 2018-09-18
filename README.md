# Performance Evolution Matrix
This respository contain the artifacts needed to replicate our experiment in the paper "Performance Evalution Matrix".



# Baseline

## Open Baseline Image.


**MacOSX.** We do all the experiments in a Mac Book Pro. To open the Baselina setup execute the following command in the folder where this project was download.

```
./Pharo-OSX/Pharo.app/Contents/MacOS/Pharo Baseline.image
```

**Windows.**
You may also run the experiment in Windows, but depending of the windows version you have installed it may be some some UI bugs.
```
cd Pharo-Windows
Pharo.exe ../Baseline.image
```

## Before & After Working Session

Before each participant init a task we execute the following script in smalltalk. It allow us to track the time that user init the experiment and how many mouse clicks, movements.
```
UProfiler newSession.
UProfiler current start.
```

After finish the task we executed the following script. It stop recording the mouse events and save the stop time.
```
UProfiler current end.
```

The last script generate a txt file with the following information: start time, end time, number of clicks, number of mouse movements, and number of mouse drags (we do not use this last one).
```
11:34:52.5205 am,11:34:56.38016 am,14,75,0
```
## Open a project

There are three projects under study, depending of the project you wanna use for the task one of the following scripts.

**Roassal**
```
TProfileVersion openRoassal.
```

**XML**
```
TProfileVersion openXML.
```
**Grapher**
```
TProfileVersion openGrapher.
```
For each project, we provide a UI which contains all the tools we use as baseline.

<img src="images/baseline.png" width="300">

- Browse: open a standar window to inspect the code of the project in the selected version.
- Profile: open a window with a call context tree for the selected version.
- Source Diff: open a window with the code differences between the selected version and the previous one.
- Execution Diff: open a window with the merge call context tree gathered from the selected version and the previous one.

# Matrix

## Open Matrix Image.

**MacOSX.** We do all the experiments in a Mac Book Pro. To open the Baselina setup execute the following command in the folder where this project was download.

```
./Pharo-OSX/Pharo.app/Contents/MacOS/Pharo Matrix.image
```

**Windows.**
You may also run the experiment in Windows, but depending of the windows version you have installed it may be some some UI bugs.
```
cd Pharo-Windows
Pharo.exe ../Matrix.image
```

## Before & After Working Session

Before each participant init a task we execute the following script in smalltalk. It allow us to track the time that user init the experiment and how many mouse clicks, movements.
```
UProfiler newSession.
UProfiler current start.
```

After finish the task we executed the following script. It stop recording the mouse events and save the stop time.
```
UProfiler current end.
```

The last script generate a txt file with the following information: start time, end time, number of clicks, number of mouse movements, and number of mouse drags (we do not use this last one).
```
11:34:52.5205 am,11:34:56.38016 am,14,75,0
```
## Open a project

There are three projects under study, depending of the project you wanna use for the task one of the following scripts.

**Roassal**
```
ToadBuilder roassal.
```

**XML**
```
TProfileVersion openXML.
```
**Grapher**
```
ToadBuilder xml.
```