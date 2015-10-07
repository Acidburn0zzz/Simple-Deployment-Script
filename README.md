# Simple-Deployment-Script

This simple python script can be used to manage Git-managed websites/projects on a production server.

## release.conf
Each project should contain the following file in its root directory:

    # release.conf

    {
        "projectType":  "symfony2",
        "branch" :      "release"
    }


Here are the configuration keys:


 - `projectType`

    Specifies the project type. Depending on its value, different hooks will be
    executed after the local repository has been synced.

    **Type**: `string`  
    **Values**: `symfony2` / `vanilla`  
    **Default value**: `release`


 - `branch`

    Specifies the production branch
    
    **Type**: `string`  
    **Default value**: `release`

## How to execute it
All you have to do is to run `python release.py`:

    root@server:~/deploy# python release.py
    Please select a project to sync

        [0] project1 (master)
        [1] project2 (release)
        [2] project3 (release)
        [3] project4 (pre-prod)
    ? 1
    Already on 'release'
    Already up-to-date.
    Release finished. Have an A1 day!
