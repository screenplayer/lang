# ScreenPlay language standard (Informal)

## Introduction

ScreenPlay is language for writing screen play. It has plain text formatting syntax and is very esey for computer to parsing.

## Syntax

### Defination

When writing screen play, usually authors will start with some defination, like title, author name, draft date and so on. In ScreenPlay, the format of defination is \${key}={value}. And value can be string or multiple string separate with **;**.

    ${Title}={Document of ScreenPlay}
    ${Credit}={Written by}
    ${Authorr}={Jacob Chang}
    ${Draft date}={06/20/2019}
    ${Contact}={
        mrchangji@outlook.com
        https://github.com/ScreenPlayer/lang.git
    }
    ${Characters}={Character A; Character B}

### Scene Heading

Scene Heading are strings wrapped by brackets.

    [ENT]
    [INT]
    [EST]
    [INT./EXT]
    [INT/EXT]
    [I/E]

### Characters

Character starts with **@{** and ends with **}**

    @{Character}

### Dialogue

Dialogue is started with **::**, words are surronded by **"**. For simultaneous dialogue, you can use **&&** to combine multiple dialogue or multiple characters

    @{CharacterA} "Hello, B"
    @{CharacterB} "Hello, A"

    @{CharacterA} "Hey, B" && @{CharacterB} "Hey A"
    @{CharacterA && CharacterB} "Hey"

### Parenthetical

Parentheticals are wrapped in parentheses

    @{Character}(with sad face) "Long time no see"(pause)"Where have you been"

### Transition

Transitions are start with ">>"

    >> CUT TO:

### Action

All other paragraphs will be treated as actions.
