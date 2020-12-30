# ScreenPlay language standard (Informal)

## Introduction

ScreenPlay is language for writing screen play. It has plain text formatting syntax and is very esey for computer to parsing.

## Syntax

### Definiton

When writing screen play, authors can start with definitons, like title, author name, draft date and so on. In ScreenPlay, the format of definiton is *${key}={value}*. And value can be string or multiple string separate with **;**.

    ${Title}={Document of ScreenPlay}
    ${Credit}={Written by}
    ${Author}={Jacob Chang}
    ${Draft Date}={06/20/2019}
    ${Contact}={
        mrchangji@outlook.com
        https://github.com/ScreenPlayer/lang.git
    }
    ${Characters}={Character A; Character B}

### Scene Heading

Scene Heading are strings wrapped by square brackets.

    [ENT]
    [INT]
    [EST]
    [INT./EXT]
    [INT/EXT]
    [I/E]

### Characters

Character starts with **@{** and ends with **}**, similar to what you do on social media.

    @{Character}

### Dialogue

Dialogue is started with **CharacterA**, words are surronded by **"**. For simultaneous dialogue, you can use **&&** to combine multiple dialogues or multiple characters

    @{Character A} "Hello, B"
    @{Character B} "Hello, A"

    @{Character A} "Hey, B" && @{Character B} "Hey A"
    @{Character A && Character B} "Morning"

### Parenthetical

Parentheticals are wrapped in parentheses

    @{Character}(with sad face) "Long time no see" (pause) "Where have you been"

### Transition

Transitions are start with ">>"

    >> CUT TO:

### Action

All other paragraphs will be treated as actions.
