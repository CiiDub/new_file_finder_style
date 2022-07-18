# New File - _Finder Style_

This is an [Alfred](Alhttps://www.alfredapp.comfred)  workflow that makes a new text file in the style of the Mac Finder.

This version requires Alfred 5

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

Hint: Because the file is selected in the Finder __⌘↓__ will open the file in it’s default app.

![Animated Gif of the workflow in progress](nf.gif)

![Layout of workflow. ](layout.png)

New File _Finder Style_ also has an external trigger. This allows the workflow to be triggered from Applescript. With the trigger ID of __trigger.nf__ from the workflow ID of __com.buttergut.nf__

```AppleScript
tell application id "com.runningwithcrayons.Alfred"
	run trigger "trigger.nf" in workflow "com.buttergut.nf" with argument "test"
end tell
```

Hint: I used this to make the New File Button in the Finder. Just drop the “with argument...” bit at the end of the line and it defaults to “untitled”.

You can take a look at the button here: [New File Finder Button](https://github.com/CiiDub/new_file_finder_button)

![New File Finder button](finder_button.png)