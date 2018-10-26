# Week 8

## Installed anaconda
This was quite tricky to do given the group permissions on the remote machine. We wanted it such that we have one install that all users can use, rather than each of us installing anaonding and each keeping the our microscopium installs up to date / in line. To make things more confusing, there was an install of anaconda in a separate user's home folder that I was able to access simply by quering conda --list.
Eventually conda was installed and all users are able to use it from the one location, with each user having a different environment.

## Installed microscopium
This made installing microscopium a lot cleaner, as we were able to simply `pip install --upgrade -e --no-deps .` Note the lack of sudo. This also means if we make any changes to microscopium locally, the fact that we installed with -e means these changes will immediately be reflected in any of our scripts without us needing to reinstall.

## Ran a trial/demo from the machine
Our script now runs with the directory structure on machine. The task now is to tweak the script to work over the multiple directories. This shouldn't be too much work, but it will take some time, particularly since there were some images in the test data which were corrupted/not useable. We will have to weed these all out.

## Pull request
After making a couple of changes to our pull request it has been accepted! How cool.


