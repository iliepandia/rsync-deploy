# Zero downtime code deploy - SSH - rsync

Basic script that will deploy your code to a remote SSH server with zero downtime.

The basic steps are:

- use rsync to upload your code to a new build folder, using the current time as a suffix
- once the upload is complete, use a link to point to this new folder

With this procedure, your app will switch to the new code instantly, even if the initial 
upload takes more time. 

## Rolling back

Rolling back is as simple as moving a link back to a previous deployment folder

## Improvements

The script should be updated to remove previous deploys, keeping only the latest <n> deploys
available.
