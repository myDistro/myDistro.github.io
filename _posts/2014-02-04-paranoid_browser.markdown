---
layout: post 
title: paranoid_markdown
status : alpha
subtitle : that plugin sets up the configuration that lets you start your favorite browser as another user, so the browser can't ready you .ssh and gpg keys.
---

for example do

    class { 'paranoid_browser': }
    paranoid_browser::user { 'me':    user => 'palo' }
    paranoid_browser::user { 'myMom': user => 'mom' }
