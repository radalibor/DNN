** Prerequisites **
*******************

1. IIS 7+.
2. SQL Server 2008 R2+.
3. VS2015+ (Community Edition Supported).
4. .Net Framework 3.5. This is needed for few modules.
5. .Net Framework 4.5+.
6. Internet access to automatically download nuget packages from nuget.org.
7. Java for YUICompressor to run during compile.


** Compilation Steps **
***********************

1. Prior to compilation, have a look inside Platform\Website\Install\Module folder. It should have 21 files.
2. It's best to keep this folder open all the time so you can see when new files are added here.
3. Open the following solutions one by one in Visual Studio and compile in RELEASE mode.
   -- Dnn.Platform\DNN_Platform.sln
   -- PB.Lib\src\Dnn.PersonaBar.Lib.sln [OPTIONAL]
   -- PB.Ext\src\Dnn.PersonaBar.Ext.sln [OPTIONAL]
   -- EditBar\src\Dnn.EditBar.sln [OPTIONAL]
4. This will create several new zip files under Dnn.Platform\Website\Install\Module folder. 
5. Ensure you have 48 zip files and 1 placeholder.txt in the above folder.
6. The compilation of the last 3 solutions are optional as the zip files from them are already included in the above 21 files mentioned.
6. If you see fewer files, then ensure that the ALL compiles were done in RELEASE mode. 
7. There should not be any ERRORS in compile. Warnings can be ignored.


** Site Setup **
****************

1. Under IIS, configure a site and point to the full path corresponding to Dnn.Platform\Website folder.
2. Ensure that the user running the app pool has read and write permission to this folder.
2. Start the site.
3. DNN Install Wizard should show up shortly.
4. Create a new database in SQL Server and provide it's name and credentials to the wizard.
5. Wait for site to finish installation.
6. Login as username: host and password: dnnhost.
7. The Admin Experience panel slides out on the left.
8. Create pages, users, content, etc.

** Enjoy DNN **
:)

http://www.dnnsoftware.com/
