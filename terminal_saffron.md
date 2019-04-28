###Terminal Tips  
  
* Open Ports (Listening):  
	$ netstat -plunt  
* Open Ports (ALL):   
	$ netstat -nap  
* Show files/folders in a website index directory:   
	$ chown to the website user:group.   
	for symlinks use $ chown -h without ending slash!  
* Deluge errors?   
	check the owner of folder Downloads/.  
* Directory size:   
	$ du -chs  
* Copy to clipboard (OS X):  
	$ pbcopy < FILENAME  
* List of available printers over network (e.g. agate):   
	$ lpstat -t   
* Remove duplicates w/ sort:  
	-u: unique  
	-o: output to a file instead of stdout  
	$ sort -u -o PATH_TO_FILE PATH_TO_OUTPUT_FILE  
* Favorite tar command:                            
	$ tar -xvf FILE_PATH --checkpoint  
* Timing in terminal, in front of your command (like sudo):  
	$ time  
* Deleting a specific line by line-number in a file and get a backup of the original file:  
	$ sed -i.babak -e 'LINE_NUMBER_d' FILE_NAME  
* Counting number of lines in a file:  
	$ wc -l FILE_NAME  
* Print a specific line on screen by line-number:  
	$ sed -n 'LINE_NUMBER_p' FILE_NAME  
* Counting instance of a string in a file:  
	$ cat FILE_NAME | grap -c 'YOUR_STRING'  
* Bring a currently running process to background and cut the dependency on the shell instance:  
  	CTRL + Z to pause it  
	$ bg  
	$ fg  
	$ jobs  
	$ disown -h %JOB_NUMBER  
* Execute a long job in the politically right way:  
	$ nohup nice bash -c "COMMAND" &  
* Find text in a path (Grep):  
	-n: line number  
	-i: case insensitive  
	-r: recursive - prints the lines  
	$ grep -nir <PATH> -e "TEXT"  
* Find a filename:  
	$ find PATH -name FILE_NAME  
* rsync via a specific port:  
	-P: Progress  
	-r: recursive  
	-v: verbose  
	-z: compress(zip) during the transfer  
  
	-e: execute  
	$ rsync -Prvz -e 'ssh -p 2281' ./FILE_NAME USER@HOST:PATH  
* Zip compressing:  
	$ zip -v  
* Columns of a text file:  
	$ cat FILENAME | awk '{print $COL_NUM}'  
* Print to stdout:  
	$ printf = $ echo  
* Clear the buffer:  
	$ printf "\033c"  
