Android backup extractor
========================

Utility to extract and repack Android backups created with adb logcat (ICS). 
Largely based on BackupManagerService.java from AOSP. 

Usage: 

Drop the latest Bouncy Castle jar in lib/, import in Eclipse and adjust 
build path if necessary. Use the abe.sh script to start the utility. 
Syntax: 

	unpack:	abe.sh unpack <backup.ab> <backup.tar> [password]
	pack:	abe.sh pack <backup.tar> <backup.ab> [password]

If you don't specify a password the backup archive won't be encrypted but 
only compressed. 

Alternatively: 

Use to bundled Ant script to create a an all-in-one jar and run with: 

java -jar abe.jar pack|unpack [parameters as above]

(Thanks to Jan Peter Stotz for contributing the build.xml file)

More details about the backup format and the tool implementation in the 
associated blog post: 

http://nelenkov.blogspot.com/2012/06/unpacking-android-backups.html
