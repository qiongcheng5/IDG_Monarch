1. Database installation
   [C:\Users\Qiong\chunting\projects\MonarchApp\prj\scripts\database_auto, originally at C:\Users\Qiong\chunting\mysqlbox]
   [Associated data at C:\Users\Qiong\chunting\data\systemsbiology]
   1.a) Monarch_DTO_DB_Creation.sql  
   1.b) Monarch_DTO_DB_Data.sql
   
   1.c) Backup database
        mysqldump -u root -p monarch_dto > monarch_dto.sql
   1.d) Restore database
        mysql -u root -p
			mysql> create database monarch_dto;

        mysql -u root -p monarch_dto < monarch_dto.sql
        
   [Refer to http://www.thegeekstuff.com/2008/09/backup-and-restore-mysql-database-using-mysqldump]

2. Dependent software 
   2.a) cURL
   cURL is a lightweight, command-line tool for making HTTP requests without a web browser. cURL lets you try out various API requests in a command-line interface such as the command prompt in Windows or Terminal on the Mac. You don't need to build a working web application just to try out the APIs.
   
   2.a.1) Install cURL in windows
     - Go to http://curl.haxx.se/download.html and download the executable file
     - Unzip it and add its bin subdirectory path into the system environment variable PATH
     - Go to http://curl.haxx.se/docs/caextract.html and download the digital certificate file named cacert.pem to its bin subdirectory path
     
   2.a.2) Check whether cURL has been installed in Linux/MacOS by default
   
   2.b) Git
   2.b.1) Download from https://git-scm.com/download/win
   2.b.2) Use the Git Bash to manage the versions for the repository at https://github.com/qiongcheng5/IDG_Monarch.git
   
		…or create a new repository on the command line
		
		Copy to clipboard 
		echo "# IDG_Monarch" >> README.md
		git init
		git add README.md
		git commit -m "first commit"
		git remote add origin https://github.com/qiongcheng5/IDG_Monarch.git
		git push -u origin master
		
		…or push an existing repository from the command line
		
		Copy to clipboard 
		git remote add origin https://github.com/qiongcheng5/IDG_Monarch.git
		git push -u origin master
		
		
		…or import code from another repository
		
		You can initialize this repository with code from a Subversion, Mercurial, or TFS project.
   
3. Configuration
   3.a) Change the basedir property in the file config.properties at the subdirectory src\dto\util
   3.b) Change the database settings in the file db.config at the subdirectory src\dto\util
# IDG_Monarch
