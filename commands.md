# Linux Commands

Create a tar file:

             tar -cvf filename.tar nameofFolderNeedToCompress

Extract a tar file to a current directory:

             tar -xvf file.tar
             
change owner of file/directory:

            $chown [new owner name]  [file name/ directory name]

change groups user:

            $chgrp [group/user name] [file name/directory name]

Install deb file:

            $sudo dpkg -i [package name]
            $sudo apt-get install -f 

git commit:

            $git commit -am "message"
            
git reset:

            $git reset --hard <commit>
            reverts code back to a previous commit
            $git reset --hard origin/master
            reverts code back to remote repository version
            
git branch:

            $git branch <branch_name>
            create a new branch with its name
            switch to this branch
            $git checkout <branch_name>
	    
	    git checkout <your branch name>
	    #check if you are on your branch
	    git branch 
	    #commit your changes then push it to your branch(not the master branch) using this command
	    git push --set-upstream origin <your branch name>
            
git merge:
            $git merge <branch_name>
            merges this branch to master ( the current branch)

            after merging we can delete the branch:
            $git branch -D <branch_name>
            
change owner group:

            $whoami
            $id -gn
            username of current user, the primary group name of user.
            $sudo chown –R [Username]:[Groupname] /opt/lampp/htdocs
            only for htdocs directory.

Change the whole Xampp configuration to current user not root by default:

            make a back-up file:
            $sudo cp /opt/lampp/etc/httpd.conf /opt/lampp/etc/httpd.conf.back
            open and edit httpd.conf, change user and group to your current user 
            and group you want and save it.

            testing if Xampp working perfectly:
            $sudo /opt/lampp/lampp restart

            $sudo /opt/lampp/lampp status
            
switch form git remote https to SSH avoiding enter credentials

            check: $git remote -v
            switch: $git remote set-url origin <SSH link>

open File Browser for current Path:

            $nautilus .

completely remove mysql:

            $sudo apt-get remove --purge mysql-common mysql-client mysql-server

Make Deployd App: installation: 

            $ sudo apt update
            $ sudo apt install -y mongodb
            $ sudo systemctl stop mongodb
            $ sudo systemctl disable mongodb
            $ npm install deployd-cli -g

            make a app:

            $ dpd create app-name
            $ cd app-name
            $ dpd -d

Transfer Keybase to a new machine:

            1. Install keybase to new machine:
             (go to keybase.io for instruction)

            2. Login to keybase on the new machine
                keybase login

            3. Select the device for authentication
            4. Confirm the new device added on the original machine

            5. Transfer public key to the new machine
                keybase pgp export | gpg --import
                
            6. Transfer private key:
                keybase pgp export --secret | gpg --allow-secret-key-import --import

Install NodeJs:

        1. 
            sudo npm install npm -get
            sudo chown -R henry:henry /usr/local/lib/node_modules
            sudo chown -R henry:henry /usr/local/bin/
            sudo chown -R henry:henry /usr/local/share/
        2.
        
            Create a directory using the command mkdir ~/npm-global
            Configure npm to set the directory using the following command npm config set prefix ~/npm-global/
            Create a file named ~/.profile and add the path export PATH=~/npm-global/bin:$PATH
            Type reset in the terminal
            
Install Foundation

            1.Install Foundation command line in npm using npm install -g foundation-cli
            2.Go to ~/Github directory (or the directory for your projects) and run foundation new.
            3.Choose "A site" as the installation
            4.Enter your site name and choose ZURB Template
            5.Change directory ~/Github/your-web-site

Install Firebase

            1.Install firebase command line using npm install -g firebase-tools
            2.Run firebase init and enter your-web-site name.
            3.Run npm start, and it will populate the dist folder with your site.
            4.Choose dist as your main directory for Firebase.
            5.Install a local server using npm install -g serve.
            6.Run serve dist to indicate that you're referring to the Foundation compiled site.
            7.Try to access Firebase in your localhost. For example, localhost:3000.
            
Deployment

            1.Run firebase deploy
            2.Run firebase open to open your site automatically.

Configure git for sign commit option:

            git config --global user.signingkey [your gpg/pgp key from keybase]
            git config --global commit.gpgsign true  
            (sign every commit, optional)

Edit config file for git:

	    git config --global -e
	    git config --system -e
	    git config --local -e

Complete remove :

	    sudo apt-get purge [name] && sudo apt-get autoclean 

set up firebase-react:

            npm install firebase --save
            npm install -g create-react-app
            npm install -g firebase-tools
            npm install firebase --save
            mpm install --save react-router
            npm install react-router-dom
            create-react-app my-app  
            cd my-app
            npm start  
List contents of another directory without being in the current of directory:

	    ls  /usr/bin
	    
List all files in a directory including hidden file:
            
	    ls -a
	    
Rename the file while copy:

	    cp .bashrc temp2/.bash
	    
Remove directory:

	    rmdir <dir name>
	    
List contain of Parent Directory:

	    ll ..
	  
Rename file:

	    mv <current name>  <new name>
	    
copy a file into a directory:

	    cp <file name>  <directory name>
	    
Search for a string "student" in all the files in the /etc directory:

	    grep student /etc/*
	    or grep -s student /etc/*  
	    
Display all processes are running:

	    ps ax
	    
Kill a process with PID:

	   kill -9 <#pid>
	   
To show current user log in:

	   who or whoami
	   
Show the history commands we have entered:

	   history
	   
Determine whether a remote system is responding to low-level network activity:

	   ping google.com
	   ctrl +c 
	
Set up Flask:

	   pip install virtualenv
	   mkdir projectName
	   cd projectName
	   virtualenv venv
	   source venv/bin/activate
	   pip install Flask
	   
	 

		
