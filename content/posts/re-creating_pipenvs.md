---
title: "Re-creating pipenvs"
date: 2022-08-23T13:48:37-07:00
tags: []
draft: true
---    
Upgrading an operating system isn't the best idea for a resilient setup. 
When I did (just to see what would break), my python setup was broken. 
There was likely a broken symlink somewhere deep. 
Here was the quickest way to fix it.
Remove the pipenv and recreate it with the explicit python to be used.


    cd ../Projects/project-name/                                                                            
    pipenv --rm                                                                                     
    pipenv --python /usr/local/bin/python3.10                                                       
    pipenv shell  
