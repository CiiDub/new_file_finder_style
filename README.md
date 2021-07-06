# New File - _Finder Style_

This is an [Alfred](Alhttps://www.alfredapp.comfred)  workflow that makes a new text file in the style of the Mac Finder.

__It works with three commands:__

1. New File
2. nf
3. ⌘ ⌥ N

These will each create a text file in the front most open folder or on the Finder desktop.

__It follows Finder rules.__

The default name of the file is “untitled”.

__⌘ ⌥ N__ can not take a parameter so the file will be created, with it’s name “untitled” selected. Just start typing to change it.

__New File__ & __nf__ can take a name as an optional parameter. So `nf magnum opus.txt` will create a file name “magnum opus.txt”.

If you make a file with a name that is already in use in that folder the name will be appended with “ 2”, then “ 3” and so on. 

It respects your file extension while dealing with duplicates. So if  “magnum opus.txt” exists  then “magnum opus 2.txt” will be created.

Magnum Opus 2 will be -obviously I think- the title of my memoir.

Hint: Because the file is selected in the Finder __⌘↓__ will open the file in it’s default app.

New File _Finder Style_ also has an external trigger. This allows the workflow to be triggered from Applescript. With the trigger ID of __trigger.nf__ from the workflow ID of __com.buttergut.nf__

```AppleScript
tell application id "com.runningwithcrayons.Alfred"
	run trigger "trigger.nf" in workflow "com.buttergut.nf" with argument "test"
end tell
```

Hint: I used this to make an Automator Quick Action, so that I can have a button to make text files from the Finder. Just drop the “with argument...” bit at the end of the line.

![Animated Gif of the workflow in progress](nf.gif)

![Layout of workflow. ](layout.png)

![Quick Action in Finder. ](quick_action.png)