Siza Adhikari 
----
This is assignment 1.
----
April 28, 2023 
----




Question and Answer 
----



a. Can we have a global .gitignore file?

    Yes, we can have a global git ignore file.


b. How to find the difference between two commits?

    We can find the difference between two commits by using the "git diff" command. 

-----

  Example:
------
    PS F:\8thsem\internship\gitlesson_1> git log --oneline
    b672704 (HEAD -> master, origin/master) new changes in the file
    fd769f4 new file
    ae0d952 redo
    11907a7 new file updated
    a92eff3 adding new files
-------
    PS F:\8thsem\internship\gitlesson_1> git diff 11907a7 a92eff3
    diff --git a/file.txt b/file.txt
    index 94674de..e69de29 100644
    --- a/file.txt
    +++ b/file.txt
    @@ -1 +0,0 @@
    -It's my first time writing here! 
------

c. Write difference between git add and git commit commands.

    The main difference between the git add and git commit commands would be in the:
    When, we perform the command git add, it means we are sending it to the staging area of the git workspace. 
    And, when we perform the command git commit, it means now we are sending it to the git repository. 

    So, when we perform the git add command, we are telling the git that, we have either new files or modified files with us,
    which we are ready to track and upload it. 
    And, when we perform the git commit command, we are telling the git that, we have already added the files which we wanted to 
    either track or upload now we are ready to put the changes into the repository. 

 d. How to unstage files?

    Unstaging the files means that we are taking it back to the initial phase i.e. brining back from the staging phase.

    For, unstaging the files, we perform:
-----
               git restore -- staged "filename"
            OR,
                git reset "filename"
-----                

e. How to revert a commit?

    Reverting a commit means making it seem like I have never ever added anything like that. So, to revert a commit the command,
    to be used would be:

        git revert "SHA code/7 digit code of the commit which you want to revert back"

    Example:

    git log --oneline
    b672704 (HEAD -> master, origin/master) new changes in the file
    fd769f4 new file
    ae0d952 redo

    PS F:\8thsem\internship\gitlesson_1> git revert a92eff3


f. Difference between revert and reset.

    If I want to remove a commit from the history of a repository or if I want to start over from a previous state at that time I will be using the git reset command.


    But, if I want to undo a commit that has already been pushed to a remote repository and has been shared with others I will be using the git revert, since it will be making it seem like I had never pushed such commits to the repo.







