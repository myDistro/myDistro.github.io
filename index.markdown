---
layout: default
title: Build you own Distribution
subtitle : secure as you like it once and use it as often as you like
---

my Distribution 
----

This project is like [boxen](http://boxen.github.io) but with another target.
Linux and other Unix systems most of the time come with a very good supported package managment system.
So why don't create a bund of puppet recipies to configure your laptop once and spread it multiple times.

We don't have an interface or something right now, actually you don't need one. 
Right now there are just 2 small basic ideas to make configuration easier.

[configuration](http://github.com/myDistro/configuration)
----

can be used to save configuration files like vim and .i3 in a gitrepository and share them (naturally by git) between computers.
right now there must be a setup.sh script in the repo but this will change soon.

    puppet module install myDistro/configuration

you can use it than

    configuration { "palo-shells":
        target => '/home/palo/spread-shell',
        source => 'mrVanDalo/spread-shell',
        user   => 'palo',
    }

[paranoid browser](http://github.com/myDistro/paranoid_browser)
----

that plugin sets up the configuration that lets you start your favorite browser as another user, so the browser can't ready you .ssh and gpg keys.

    puppet module install myDistro/paranoid_browser

for example do

    class { 'paranoid_browser': }
    paranoid_browser::user { 'me':    user => 'palo' }
    paranoid_browser::user { 'myMom': user => 'mom' }
