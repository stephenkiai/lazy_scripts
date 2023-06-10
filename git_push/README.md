# git add; git commit; git push

```To automate  the above steps:
      >>> open terminal
      >>> create a file name it 'push' or whatever name you like,
      >>> then type the following inside the file you just created:
      
      	      >> #!/bin/bash
	      >> git add .
	      >> git commit -m "${*:1}"
	      >> git push
```
```
>>> This line uses the git commit command to create a new commit with a
>>> commit message. The -m flag is used to specify the commit message.
>>> ${*:1} is a parameter expansion that represents all the command-line
>>> arguments passed to the script, except for the script name itself ($0).
>>> In this case, it takes all the arguments ($*) starting from the first one (:1)
>>> and uses them as the commit message.


```
```
      >>> now save and make the file executable using command:
      	      >> chmod u+x filename
```
      >>> run it from the command line like this:
      	     >> ./filename "Commit message"
```
	      
      >>> but since we want to be lazy as much as possible,lets avoid
      >>> creating this file every time we want to use it in our current
      >>> working directory by:
      
      	      >> sudo mv filename /bin
	      >> The /bin directory is one of the standard directories in
	      >> the Linux file system hierarchy and is typically used to
	      >> store essential command-line utilities and executable programs.

      >>> To use the script just type your filename+space+your commit message. i.e;
      	      >> filename commit message
```
```
 >> By moving a script to the /bin directory, you make it
 >> accessible from anywhere in the system, allowing you to
 >> execute the script by simply typing its name in the command
 >> line, without specifying the full path to the script.
```
```
:: CAUTION
>>> Keep in mind that moving scripts to system directories like /bin should be
>> done with caution, as it may affect system stability or security if not done
>> properly. It's generally recommended to keep user-specific scripts in a
>> different directory, such as /usr/local/bin or your home directory's bin folder.
```
