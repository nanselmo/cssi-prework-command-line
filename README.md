
#Intro to the Command Line

### Key Terms
* `Terminal` : A text-based tool that allows you to communicate with your computer. The user types a line of text into a simple prompt, and the computer runs that command. On OS X your terminal is an application appropriately called Terminal. <br>
* `Graphical User Interface` : A graphical display that allows you to communicate with your computer through icons and other visual elements like pointers, folders


#Motivation?
Back in the day (the 1980s!), computers only had a terminal to control them. The terminal is a text-only way to communicate with your computer. Later on, Graphical User Interfaces (GUIs) were created to make computers more accessible and intuitive for those who weren't as computer savvy. Developers continue to use the terminal instead of the GUI because once you get the hang of it it's quick and provides a lot of features.

##Opening the Terminal
+ By Using Spotlight Seacth - On a Mac, access Spotlight Search by clicking the magnigying class in the upper right navigation bar or by pressing Command + Space. Then search for terminal and press Enter.


## Navigation

Open up command prompt or terminal. The `pwd` command stands for "**p**rint **w**orking **d**irectory". Type in: `pwd` and hit return.

You will see the names of the folder and subfolders that you are currently in. These folders are called directories. 

`/Users/avi` 

**Note:** `avi` *is my username; your own username will appear here.*


`/User/avi` means I am in a directory called `avi` and that directory inside the `User` directory. Since there are no other directories listed before `User`, `User` must be at the root, or start of my file system.

 `/User/avi` is my home directory. It belongs to the user I am currently logged in as. The placeholder for a user's home directory is the `~` ("tilde") symbol.

Try this:

**Note:** *Any time you see the* `$` *character, you shouldn't type it in. This is just a standard way to represent a command line prompt. Yours may or may not be a* `$`.

```bash
$ cd ..
$ pwd
```

You should now see that you are one directory above where you were, in my case

`/Users`

The `cd` command stands for "**c**hange **d**irectory".
The `..` is a placeholder meaning the directory above the working directory.

Try this:

```bash
$ cd .
$ pwd
```

You can see you are still in the same directory.

The `.` is a placeholder meaning the current directory.

So here are three default placeholders for your file system:

- `~` Your **home** directory
- `.` The **current** directory
- `..` The directory in which your current directory is contained—referred to as the "**parent**" directory.

You can supply any path to the `cd` command to navigate to that location.

Try this:

```bash
$ ls
```

You should see a list of all the files within your working directory.

The command `ls` stands for "**l**i**s**t".

Try this:

```bash
$ cd /Users/avi
$ pwd
```

The working directory is back to `/Users/avi`.

## Paths

The path supplied to the `cd` command, for example `/Users/avi`, is known as an absolute path.

Systems can use either *absolute* or *relative* paths.

An absolute path is a path that points to the same location on the file system regardless of the working directory. They start with `/` ("forward slash") because that is the root of your file system.

This is an absolute path: `/Users/avi`.

A relative path is a path **relative** to the working directory of the user or application, so the full absolute path will not have to be given. They start with the name of a directory or a file.

This is a relative path: `avi/Documents`.

Paths use `/` to denote levels.

How many levels are within the following path?

`/Users/avi/Development/code/flatiron-school/mixtape-app`

- [The One True Path](http://blog.seldomatt.com/blog/2012/10/08/bash-and-the-one-true-path/)
- [More on paths - Wikipedia](http://en.wikipedia.org/wiki/Path_\(computing\))

Knowing where you are in your terminal - what directory you are working in - is very important.

(If you said 6 levels to the question above you are right!!)

## Commands

Another cool command you can you use is `touch`, which simply creates a new file. Try:

```bash
$ touch hello_world.py
```

Now try:

```bash
$ ls
```

You should see the file you just created, `hello_world.py`, in the working directory. Note that this is an empty file and has nothing inside of it, because you just created it.

From within a shell you can also execute programs. Navigate to where you saved your `hello_world.py` file and try:

```bash
$ python hello_world.py
```

This command is no different than the `cd` command. We're executing the `python` program by supplying a path to a file to execute. Because the `hello_world.py` file you just created is completely empty and has no contents inside of it, there is no program to run and your terminal won't actually produce any output when you tried running it via `python hello_world.py`.

The `open` command is interesting because it will trigger the default action associated with the file type. So `$ open .` will popup a finder window with the current directory in finder (because remember that `.` is an alias to the current directory). Entering `$ open hello_world.py` will open that file in your default editor.

## Tab Completion

As you type in commands you can use tab completion. Tab completion allows the shell to be smart and to try and guess what command you want to run when you hit tab.  If there's only one logical way to complete your command it will auto populate, or will show you the possibilities and you can keep typing more letters until you can tab complete your command.

For example let's say we have the following directory structure:

```bash
/flatiron_school
/flatiron_building
```

If I'm in my root directory (typing `pwd` gives me `/Users/avi`) and I type `$ cd f` and then hit tab, it will fill in everything up until the conflict so I'll see `$ cd flatiron_`.  If I then add the `s` and hit tab it will fill in `$ cd flatiron_school` and I can hit enter.



## More Resources:

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Environment Variables](http://cbednarski.com/articles/understanding-environment-variables-and-the-unix-path/)
- [Built-in Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html) *Very useful*
- [15 Useful Bash Commands](http://www.thegeekstuff.com/2010/08/bash-shell-builtin-commands/)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/bash-tutorial' title='Intro'>Intro</a> on Learn.co and start learning to code for free.</p>


#Tips and tricks:
If you start typing a directory name or file name you can click `Tab` and the command line will automatically fill in the rest of the directory/file name. If you click `Tab` twice it will show you all of the directories/files inside your current directory.
Navigating your computer from the command line is a lot about muscle memory. The more practice you have the faster you will get!
If you need extra support, you can watch the video below. It will walk you through the basic commands that you will use day to day as you learn to code.

<iframe width="640" height="480" src="//www.youtube.com/embed/s5S_2BdrMJE?rel=0" frameborder="0" allowfullscreen></iframe>


#Conclusion
As we learn to build complicated applications, being able to swiftly navigate your computer using the command line will make your life much easier. The command line will be important not just for navigation, but you'll also use it to do things like boot the local server for your web apps, write scripts to automate tasks, and execute other important functions on your computer.
