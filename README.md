# Aggressor Scripts

### File Viewer

- Right click a file in the File Browser and select View

- ~If the file size is greater than 200mb, it tells the user that this is probably a bad idea and might cause things to crash.~
	
	- the sleep sizeof() function does not return size in bytes as specified in the documentation so there's no way to do this.

- First aggressor script so go easy on me. Sleep is a horrible, horrible language.

### Cat

- Simple alias "cat" since its better opsec than "shell type"

- Uses primary token, does not inherit beacon's thread token according to bexecute_assembly documentation

#### Problems

- FileViewer

	- ~deleteFile doesn't work for some reason when I'm trying to clean up. Returns '1' which is undocumented behavior.~

		- Fixed

	- The drow_text_big UI element includes this extra padding on the right side of the window when you drag to maximize for some reason.   
    
    - Unless I put a show_message() right after bdownload(), you need to press 'View' a second time for the file content to appear. 

- TODO:

    - Add a ctrl-f bind and input window to allow keyword searching
