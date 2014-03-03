---
layout: post
title: configuration
status : alpha
subtitle : to use github for .dot config files
---

This module allows you to save and share your config files by using github (or other git repository provider).

Right now you need a setup.sh file in your repo.
For example :

    configure-vim
    ├── bundle
    │   └── vundle
    ├── README.md
    ├── setup.sh
    └── vimrc


After you created your github repository like described you can set it up in puppet via 

    configuration { "palo-vim":
        target => '/home/palo/.vim',
        source => 'mrVanDalo/configure-vim',
        user   => 'palo',
    }
