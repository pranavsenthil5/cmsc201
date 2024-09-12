# HW0 Grading
1. Log into GL
2. In your home directory, create a symbolic link (shortcut) to easily navigate into CMSC 201's grading folder
	 ```
	 cd ~
	 ln -s /afs/umbc.edu/users/e/r/eric8/pub/cmsc201/fall24/Grading CMSC201_Grading
	 ```

3. Navigate to the grading folder
	```
	cd CMSC201_Grading
	```
4. Navigate into the current assignment
	```
	cd HW0
	```
5. Navigate into the folder with your username. You will then find all the students in your discussion section.
6. Navigate into the first student's directory. Here you will see all the files submitted by the student and two other files - `Makefile` and `rubric.txt`.  As the students were only required to submit `hw0.py`, there should only be three files. 
	```
	[pranavv1@linux4 btinpaw1] ls
	hw0.py  Makefile  rubric.txt
	```
	`hw0.py` is the file submitted by the student
	`Makefile` is .. well... a Makefile. This has a few commands that will help you with grading the current student's submission.
	`rubric.txt` is the rubric that will be filled out and sent to the students through an email.
7. Go through the student's submission. You can use `cat`, `more`, `nano`, `emacs` or whatever you prefer. As TAs generally have more privileges than students, it is important that we go through all the files they have submitted to make sure they do not have any forbidden/malicious code before we run them.
8. Go through `rubric.txt` carefully to familiarize yourself with the rubric. Please note these are formatted in a particular way, and you should not modify them if you don't know how they work.

	  Each rubric has multiple parts - usually one for each file they submit and one for following overall guidelines. If you notice carefully, each part has lines that start with `&`. This is a placeholder and will be replaced by a number depending on what you will be giving them as the grade for that particular part of the rubric.
	  
	In the `rubric.txt`, `%%%` represent comments and the respective lines will not be shown to the students when the emails are sent. 

	The last part - for following overall guidelines - doesn't have placeholders. You are supposed to uncomment, or remove the  `%%%`, if you want to penalize them for any forbidden code. 
	
9. Go through `Makefile` to familiarize yourself with the commands. It is okay if you don't understand any of it, we will you explain the basics in the rest of the guide.
10. Run the following command in the student's directory -  `make run`. It will first show you what the expected output is and followed by the student's output.

	Here is a sample output:
	```
	[pranavv1@linux4 btinpaw1] make run
	======== PART 1 ========
	Correct solution (What you should have):
	This is going to be a great semester!
	@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
	What the student has:
	This is going to be a great semester!
	```
	For HW0, it is okay if the output does not match. We just want them to print something.
11. If everything is correct, run `make fill 1` to fill part 1 with the maximum points or `make fill` to fill the entire rubric with the maximum points. 
	
	*Note: `1` here is the part number and this will not work for the last part (for following guidelines)*
	
	If you want to give them a zero for part 1, you can do `make zero 1`. If you want to give the student a zero for the entire assignment, you can do `make zero`.
12. Please edit the rubric (only the numbers) if you want to give partial points within a particular part. You can also uncomment in the last part to penalize them for any forbidden code (global variables, libraries, list comprehension, etc.)
13. To leave comments to a student, do so in the last section of the rubric. You have to write them within the opening and ending stars.
14. Save the `rubric.txt` and close it
15. Go to the next student's directory and repeat steps 7 to 14.
16. Repeat step 15 until you are done with all the students in your section
17. If you want to check the progress of you grading, you can run `make compile` inside one of the directories with the Makefile. You will know when you are done! :)

	


