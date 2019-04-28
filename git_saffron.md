### Git Tips  
  
* Undo last commit(s):  
$ git commit -m "Something terribly misguided"          
$ git reset HEAD~                                   
<< edit files as necessary >>  
$ git add ...    
$ git commit -c ORIG_HEAD   
  
* Commits waiting for push: $ git log  
* Undo pushed commit:   
    1. $ git reset <LAST_STABLE_COMMIT_HASH>  
    2. finalize your edits. do whatever you wanted to do.  
    3. $ git commit -m "MESSAGE"  
    4. $ git push -f <REMOTE_NAME> <BRANCH_NAME>  
