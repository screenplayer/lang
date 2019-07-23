# ScreenPlay language standard (Informal)

## Introduction

ScreenPlay is language for writing screen play. It has plain text formatting syntax and is very esey for computer to parsing.

## Syntax

### Meta data

When writing screen play, usually authors will start with some meta data, like title, author name, draft date and so on. In ScreenPlay, the format of meta data is key={value}. And value can be string or multiple string separate with **;**.

    Title={Document of ScreenPlay}
    Credit={Written by}
    Authorr={Jacob Chang}
    Draft date={06/20/2019}
    Contact={
        mrchangji@outlook.com
        https://github.com/ScreenPlayer/lang.git
    }
    Characters={Character A; Character B}

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

Dialogue is surronded in **"**. For simultaneous dialogue, you can use **&** to combine multiple dialogue

    @{CharacterA} "Hello, B"
    @{CharacterB} "Hello, A"

    @{CharacterA} "Hello" & @{CharacterB} "Hello"

### Parenthetical

Parentheticals are wrapped in parentheses

    @{Character}(with sad face) "Long time no see"(pause)"Where have you been"

### Transition

Transitions are start with ">>"

    >> CUT TO:
