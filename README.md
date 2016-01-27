# Gapps-Backup
Backup tool for backing up Google Apps environments. This uses the Drive API v3.


This small program was made in .NET 4.5, the purpose of it is to run as a cmd prompt that will backup your Google Apps domain. This program will read a CSV file that contains only one column, which is your useraccount@yourgappsdomain.xyz

I had a lot of trial and error with this project, so I hope others may find it useful. Please perform PRs if you're interested in improving it.

Please understand that I know the code is very rudimentary, but it's enough to get the ball rolling.

Sites of interest if you're in the same boat that I'm in: you need to setup a Google domain-wide delegation for your Google apps domain. URL for more info: https://developers.google.com/+/domains/authentication/delegation

The code I used is mainly built on what Google already gives developers and can be found at the following URL: https://developers.google.com/drive/v3/web/quickstart/dotnet

At this time, I'm mainly concerned about backing up drive documents, so that's the only scope I'm pulling from currently. I tried putting comments in the code so others' can read along and see what I'm doing. 

Known issue(s):

1. Need to check the file name, if it has an erroneous character that Windows can't read as a file name ("\",":","!", etc...) then remove/replace the character
2. All files are backed up, but the files are dumped into the root directory and not the child directories created where the files originally sit in the user's Google Apps drive.

Hope this helps others who are looking for a similar solution!
