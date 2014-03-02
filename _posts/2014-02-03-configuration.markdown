---
layout: default
title: configuration
status : alpha
subtitle : can be used to save configuration files like vim and .i3 in a gitrepository and share them (naturally by git) between computers. right now there must be a setup.sh script in the repo but this will change soon.
---

example


    configuration { "palo-shells":
        target => '/home/palo/spread-shell',
        source => 'mrVanDalo/spread-shell',
        user   => 'palo',
    }

