---
title: Git Cmds
---
## GIT commands:
im GIT Bash Terminal unter Windows (als Admin)

------------------------------------------------
+ Create a new repository on the command line

  echo "# herbsown16_11_13" >> README.md  
  git init   
  git add README.md  
  git commit -m "first commit"   
  git remote add origin https://github.com/herbbetz/herbsown16_11_13.git   
  git push -u origin master 
  
------------------------------------------------
+ ...or push an existing repository from the command line

  git remote add origin https://github.com/herbbetz/herbsown16_11_13.git 
  git push -u origin master 

------------------------------------------------
+ ...or import code 
  e.g. https://github.com/herbbetz/herbsown16_11_13/import

  Das Plus re.oben in WebIF importiert ein anderes .git in ein neues Repository.
