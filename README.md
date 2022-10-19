
**GIT Commands**

1.	**git --version**
This command describes the git version installed in the local system  
![image](https://user-images.githubusercontent.com/114802910/193420846-b4284198-202a-4371-bfcb-1ee4cbc081ee.png)

2.	**git init**
This command is used to create new blank Git repository. This is the first command that one should run on Git which converts an existing project as Git project  
![image](https://user-images.githubusercontent.com/114802910/193420840-75dfe623-333e-4f35-8f21-6e07b662075f.png)


We get below error if we donot initialize it 
![image](https://user-images.githubusercontent.com/114802910/193420834-9d868143-1018-4ee3-af0a-889cf50a8122.png)

 
**3.	git config --global user.name “<name of user>”
**4.	git config –global user.email “<user’s email address>”****

These commands help in registering the username and emailid, such that when the user commit their changes in git, it becomes clear which user has committed the changes. It helps when multiple developers are working in same project and are targeting their changes in the same branch.
![image](https://user-images.githubusercontent.com/114802910/193420829-6500632e-62f1-4eec-a873-fec97d2e3f52.png)

 

**5.	git status**

This command gives the status of untracked files in the repository. If in the repository a new file is added or the existing file is modified or a file is deleted, this command tracks the information of all the changes.
 
![image](https://user-images.githubusercontent.com/114802910/193420823-e14db6f5-ff8d-4bc3-925f-41320ae7ca5d.png)


**6.	git add <file name>**

This command adds the specific file in the working directory to the staging area.
![image](https://user-images.githubusercontent.com/114802910/193420815-9f58d210-7e3c-49c8-859a-fb5aaff482a4.png)

 

**7.	git add .**
This command adds all the changes in the working directory in the staging area. No need to specify the filename. 
![image](https://user-images.githubusercontent.com/114802910/193420804-97e2e428-03e5-4c1f-96a3-f20eab6dceec.png)

Note:  In git when we commit the code it first goes into stagging environment and when we push the changes, the only it goes into the actual repository.

![image](https://user-images.githubusercontent.com/114802910/193420799-476e286a-7581-4c7f-90fe-4ae9705ad82f.png)



**8.	git commit  -m “Check in message"**

This command helps in committing the code/file in stagging environment.
 ![image](https://user-images.githubusercontent.com/114802910/193420781-96a56a28-99cf-4140-8cc6-600598535f12.png)


9.**	git branch**

This command let user create, list, rename, and delete branches

9.1. **git branch – lists all the branches**
 
Note : By default master is the local branch but in git the default branch is main, so before pushing changes in repository, we must change the branch to main using  command 	**git branch -M main**
   ![image](https://user-images.githubusercontent.com/114802910/193420769-1e714da8-d53f-4f45-925f-21b7b640ac30.png)

 - if we donot change the branch we will get below error:
    ![image](https://user-images.githubusercontent.com/114802910/193420737-23141a0d-2c9a-4ee2-83ba-ecbcdb0c4dbe.png)
                              

   The above error can be resolved using below command
   **git pull –rebase origin main**
   ![image](https://user-images.githubusercontent.com/114802910/193420732-8bd0adda-97a4-47a4-b94b-867ce2e8c708.png)

    
 9.2. git branch -d developer1 
 
      Deletes a branch
          
 9.3. git branch developer1  
      Create a branch
 
      ![image](https://user-images.githubusercontent.com/114802910/193420725-df698da5-7725-422e-978b-8d90f4cfc484.png)

 
                   
10.**	git remote add origin “<Git repository link>”**
This command is used to link the git repository in which user wants to push their local code. It helps in creating connections with other repositories.
 ![image](https://user-images.githubusercontent.com/114802910/193420429-a969c0fd-4a90-470c-a8a6-f48f23789353.png)


11.	**git remote -v**
This command lists the remote connection user has to other repositories.
![image](https://user-images.githubusercontent.com/114802910/193420305-f78c3c7c-d139-4f32-86fc-3c389c28fcc2.png)

 

12.**	git push origin main**
This command pushes the changes from stagging to main git repository
 ![image](https://user-images.githubusercontent.com/114802910/193420295-25ad1b06-4622-43b7-a044-7e5ae3af1fc7.png)

Note: While pushing the changes in my new repository I was getting below error:
![image](https://user-images.githubusercontent.com/114802910/193419904-aee5a888-85f3-46f1-852d-bc0d46646e69.png)
 
Resolution : https://docs.github.com/en/authentication/troubleshooting-ssh/error-permission-to-userrepo-denied-to-other-user
I added the other repository as my collaborator because both my repos were using the same key. After doing it I was able to push my code in the main repository.
![image](https://user-images.githubusercontent.com/114802910/193419896-ffc88be0-8696-4e61-8b86-e2f69440dc6e.png)

 

13.	** git checkout <branchname>**
 This command makes the mentioned branch as the focus branch in which developer can make the changes. For example: We have default main branch and one new branch developer 1 in which all the dev changes should go. So by default user is always on the main branch. In order to switch to the developer branch one can, use this command.
![image](https://user-images.githubusercontent.com/114802910/193419882-97eb29bf-8137-4770-b51b-972126eb9252.png)
 

14.	**git merge developer1**
This command is used to merge developer1 branch changes in main.
 ![image](https://user-images.githubusercontent.com/114802910/193419857-2a603e0d-1b38-4fc4-b23c-2391c2b945fd.png)


15.	**git log**

This shows the sequence of events performed in the repository
![image](https://user-images.githubusercontent.com/114802910/193419848-9a249c11-219f-4976-984d-4d6d19a906fe.png)

 
16.** git revert <commitid>**
this command is used to revert the changes pushed in the repository.


17.**	git clone <repository link>**
git clone is primarily used to point to an existing repo and make a clone or copy of that repo at in a new directory, at another location
 

![image](https://user-images.githubusercontent.com/114802910/193419646-0ea9ab87-895f-40fe-ab6f-ec5bccafa4a5.png)

18. git pull origin main
This command is used to pull the new changes from gitrepository to local machine

19. git remote remove origin
This command removes the origin

![image](https://user-images.githubusercontent.com/114802910/196788349-67272a1e-10be-4c39-acb2-2d150ddc2798.png)





