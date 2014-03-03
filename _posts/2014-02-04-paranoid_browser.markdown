---
layout: post 
title: paranoid_browser
status : alpha
subtitle : run suspicious programs by a dummyuser
---

This module was created following the blog post of [calium](http://calum.org/) 
[running firefox as another user using sudo](http://calum.org/posts/running-firefox-as-another-user-using-sudo).

To use it :  

    class { 'paranoid_browser': }

After that you can create a configuration in '/etc/sudoers.d' for every user who should be able to run programs via the dummy user.

    paranoid_browser::user { 'me':    user => 'palo' }
    paranoid_browser::user { 'myMom': user => 'mom' }

Right now it just puts in a preconfigured config for all the binarys that can be called by the dummyuser.
