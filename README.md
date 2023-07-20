To see which github account origin is linked , use command => git remote -v   where v is verbose
To set new repository as origin and get rid of old one use command =>  git remote set-url origin https://github.com/affuaqqi123/California_Tourism
After adding the origin, to push the code into the remote repo, use command => git push -u origin master
To add new repo, when there is no repo linked, use command => git remote add origin http://..........



How to host ur website on EC2
Connect to your ec2 from the folder which contains pem file
Switch to root user => sudo su -
Update your server => yum update -y   (always check hypen (-))
Install httpd server => yum install -y httpd
To check status of server => systemctl status httpd
Make temp directory => mkdir temp
Move to temp directory => cd temp
Copy the download zip address from code dropdown from the git folder ex: https://github.com/affuaqqi123/California_Tourism/archive/refs/heads/master.zip 
Now download the above zip file in temp folder => wget https://github.com/affuaqqi123/California_Tourism/archive/refs/heads/master.zip
To see the downloaded zip file => ls –lrt
Now unzip that folder => unzip master.zip
Now you can see the unzip folder in blue color ex: California_Tourism-master
Now move into that unzip folder =>  cd California_Tourism-master
	ls –lrt
Now move all from files to /var/www/html/ => mv * /var/www/html/
Now move to html folder => cd /var/www/html/
	ls –lrt
Always allow inbound rules for http and https source anywhere.
Now activate webserver (httpd) => systemctl status httpd
	systemctl enable httpd	
	systemctl start httpd
Now access your website 



