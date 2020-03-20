+++
date = "2018-11-11T16:10:28+05:30"
title = "How I Use Sublime Text 3"
draft = false
tags = [ "sublimetext","setup"]
categories =["Sublime Text","Setup"]

+++

![](/img/my-sublimetext-setup/st31.png)
![](/img/my-sublimetext-setup/st32.png)

SublimeText has been my goto text editor since its launch. Lately I am exploring VSCode, IMHO VSCode has got best pluggin/addon support at the moment and its getting better, though little slow in startup times , it doesnt bother much for my requirements. Hence I have decided to have minimal ST3 setup compared to earlier in favour of VSCode.

A File Icon
Material Theme
Package Control
Terminal


  SideBar Enhancements
Bracket​Highlighter

Emmet

Google’s spelling correction
DocBlockr 

HTML-CSS-JS Prettify

 Vue Syntax Highlight


Go Build
GoFmt
Gocode

SublimeLinter
    gometalinter

    SublimeLinter-pyyaml
    SublimeLinter-pyflakes
    SublimeLinter-pycodestyle
    
Git
GitGutter

requirementstxt



    SublimeLinter-json
    SublimeLinter-jshint
    SublimeLinter-csslint
    SublimeLinter-html-tidy
    
    
    
Trailing Spaces
livereload
Sublime Linter




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

Development

## Python Dev

## Go Dev

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

AdvancedNewFile
DocBlockr
Dockerfile Syntax Highlighting
Laravel Blade Highlighter
PHPCompanion
Vuetify


