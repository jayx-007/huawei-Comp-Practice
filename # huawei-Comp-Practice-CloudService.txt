# huawei-Comp-Practice
Huawei Competition Practice for Cloud Computing, A.I, Storage, BigData,etc.


------------------------------------------------------------------------------///-----------------------------------------------------------

				##LINUX COMMANDS BEST PRACTICE 2021##
---------------------------------------------------------------------------------------------------------------------------------------------
The required Operating Systems(O.S) for practicing CLOUD COMPUTING & CLOUD SERVICES
are Linux distribution O.S which are majorly:
1.CLOUDERA
2.CentOS(Red Hat Enterprise Linux)
3.Ghost OS(cloud OS)
4.CloudMe(cloud OS)
5.Ubuntu, etc.

Below are some best practice commands for Linux Terminals in order for one to master Cloud computing and its services:

COMMANDS					Description(Defination) / Usage

pwd						=>	Present Working Directory(i.e folder).

mkdir						=>	Make Directory(i.e used to create a folder, e.g:mkdir jayx007).

ls						=>	List Screen(i.e used to display  the list of content in a directory).

cd						=>	Change Directory(i.e used to navigate or change to another folder/directory, e.g:cd jayx007).

history						=>	Returns a dictionary(i.e history log) of all commands entered in a terminal over a period of time.

cd .						=>	This command takes you to current(or parent) directory.

cd ..						=>	This command takes you back to previous directory(i.e 1 step backwards the current folder).

mv						=>	This command does to funtion which are to Rename files or to Move files as shown below:
							(i.e: mv <OldName_file1> <new_Name_file1>  e.g: mv file1.txt file2.txt 
							OR: mv  [SOURCE-PATH] [DESTINATION-DIRECTORY])
			
touch						=>	This command is used to create a file with its extension(i.e: touch <file_name> 
							e.g: touch RubyFile.txt).

nano						=>	This commaned is used to Open file only on terminal(i.e via only the terminal environment
							i.e: nano <file_name> e.g: nano RubyApp.rb).

open						=>	This command is used to Open  any file,folder,documents, etc.(i.e: open <file_name>)
							e.g: open helloWorld.html).
			
sudo						=>	This command is used with other terminal commands to give super-admin permission and priviledges to 							    modify a file or carry out specific taks via the terminal command line,it means Super User
							Do(SUDO).
							
-------------------------------------------------------------------------------------------------------------------------------------------------

						** -- Rename Multiple Files With the mv Command -- **
						
The mv command can only rename one file, but it can be used with other commands to rename multiple files.

Let’s take the commands, find, for, or while loops and renaming multiple files.

For example, when trying to change all files in your current directory from .txt extension to .pdf extension, you will use the following command:

for f in *txt; do
   mv -- "$f" "${f%.txt}.pdf"
done

This will create a loop (for) looking through the list of files with the extension .txt. It will then replace each .txt extension with .pdf. Finally, it will end the loop (done).

If you want more advanced features, you’ll need to use the rename command, we’re about to cover.

-----------------------------------------------------------------------------------------------------------------------------------------------------

						** -- Rename Files on Linux Using the Rename Command -- **
						
With the rename command, you will have a bit more control. Many Linux configurations include it by default. But, if you don’t have it installed, you can do it in just a minute with a simple command.

In the case of Debian, Ubuntu, Linux Mint, and derivatives:

sudo apt install rename
On the other hand, if you are using CentOS 7 or RHEL:

sudo yum install rename
And, if you are using Arch Linux:

yay perl-rename ## or yaourt -S perl-rename
Now, we can start using the rename command. In general, the basic syntax of the rename command looks like this:

rename 's/old-name/new-name/' files
It may seem complex at first, but it’s a lot simpler than it might seem.

In this example, we will create a new folder called filetorename, and using the touch command, we will create 5 files.

mkdir filetorename
cd filetorename
touch file{1..5}.txt
ls
With the last ls command, you can view the files that you created.

If we want to rename a single file called file1.txt, the sentence would be like this:

rename ‘s/file1/newfile1/’ file1.txt
If we wanted to change the extension to all files, for example, to .php. We could do it this way:

rename ‘s/.txt/.php/’ *.txt
ls
We can also specify another directory where the files you want to rename are.

rename ‘s/.txt/.php/’ FILE/PATH
We’d like to mention that rename uses a regular expression of Perl, meaning this command has extensive possibilities.

Finally, it is a good idea to check all the command options. You can view them in the terminal by executing:

rename –help
Some common examples of how to use the rename command are:

Convert filenames to uppercase:
rename 'y/a-z/A-Z/' *
Convert filenames to lowercase:
rename 'y/A-Z/a-z/' *
Replace spaces in filenames with underscores:
rename 'y/ /_/' *
Remove Rename Command
If you no longer wish to have rename installed on your system, remove it using the software manager. Or from the terminal.

For Debian, Ubuntu, Linux Mint and derivatives:

sudo apt remove rename
And for CentOS and RHEL:

sudo yum remove rename
That’s it, rename is removed from your Linux machine.

Conclusion
Renaming files in Linux using the terminal is a simple and practical task but sometimes very important. Knowing how to do it is something every server manager should know.

As we have seen, there are two commands that can do it. One is simpler than the other, but both accomplish the task.

We encourage you to continue researching these commands and improving the quality of your everyday workflow.


