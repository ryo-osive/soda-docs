Adding an existing project to GitHub 
=====================================

Using the command line
++++++++++++++++++++++


Open Your project in the respective Code Editor.
------------------------------------------------
    .. image:: git5.png

Open Terminal in code editor.  
-----------------------------

    .. image:: git6.png

     
Initialize the local directory as a Git repository.
-----------------------------------------------------

    .. code-block:: bash

       $ git init

    
Add the files in your new local repository. This stages them for the first commit.
--------------------------------------------------------------------------------------    
    .. code-block:: bash
        
       $ git add .
       # Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'. 

    .. note:: 
        Name any specific directory after example:

           .. code-block:: bash
               
               $ git add. _build -f
    

    
Commit the files that you've staged in your local repository.
-------------------------------------------------------------    

    .. code-block:: bash
        
       $ git commit -m "First commit"
       # Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again. 
    


At the top of your GitHub repository's Quick Setup page, click  to copy the remote repository URL.
----------------------------------------------------------------------------------------------------
   .. image:: git7.png


In Terminal, add the **URL for the remote repository** where your local repository will be pushed.
--------------------------------------------------------------------------------------------------   
    .. code-block:: bash
       
       $ git remote add origin remote repository URL
       # Sets the new remote
       $ git remote -v
       # Verifies the new remote URL
    
Push the changes in your local repository to GitHub.
----------------------------------------------------
    .. code-block:: bash
       
       $ git push origin master
       # Pushes the changes in your local repository up to the remote repository you specified as the origin
    

