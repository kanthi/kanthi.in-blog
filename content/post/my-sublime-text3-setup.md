+++
date = "2017-07-01T16:10:28+05:30"
title = "How I Use Sublime Text 3"
draft = true
tags = [ "sublimetext","setup"]
categories =["Sublime Text","Setup"]

+++


![](/img/my-sublimetext-setup/st31.png)
![](/img/my-sublimetext-setup/st32.png)


SublimeText has been my goto text editor since it launched  

Package Control

"spell_check": true,
"dictionary": "Packages/Language - English/en_US.dic",

emmet gtkdarkthemevariantsetter markdown-extended markdown-html-preview markdown-preview materialize package control wakatime


Trailing Spaces
livereload
Sublime Linter
https://medium.com/@akshaym91/top-sublime-text-3-packages-for-javascript-developers-3c9235c79d44#.ahkx2zyew

TOML syntax highlighting

http://www.motleytech.net/en/2015/10/30/setting-sublime-text-3-editor-programming/

Zeal
https://packagecontrol.io/packages/Zeal

MarkdownEditing
ThemeScheduler
GoTools

ColorHighlighter
http://andrejgajdos.com/my-sublime-text-packages-for-front-end-development/

http://www.paulund.co.uk/web-development-with-sublime-text-2

Shortcuts
https://scotch.io/bar-talk/sublime-text-keyboard-shortcuts

## UI


#### Theme
[Materialize](https://github.com/saadq/Materialize)
GtkDarkThemeVariantSetter


## General Configuration


## WebDev

#### Emmet

#### SublimeLinter

scsslint
jshint
jscs
csslint

#### ColorHighlighter

#### BracketHighlighter

#### Themr

#### AutoFileName

## Python Dev

## Go  Dev

## C Dev

/opt/sublimetext3 open package file to change the default build system


        //C.sublime-build
        //A sublime build system configuration file for C.
        // Compile to /tmp folder
        //Run C program in xterm

        {

        "shell_cmd": "gcc \"${file}\" -o \"/tmp/${file_base_name}\"  && xterm -fg green -bg black -hold -e \"/tmp/${file_base_name}\"",
        "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
        "working_dir": "${file_path}",
        "selector": "source.c",

        }


http://www.creativebloq.com/web-design/become-sublime-text-power-user-121518438

## Productivity

#### Wakatime
