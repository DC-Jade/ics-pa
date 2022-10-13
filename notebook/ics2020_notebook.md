[TOC]

# Basics

## pointer

1. pointer is an address

2. everything in C is an address

## [KISS(Keep it simple, stupid)](https://blog.sciencenet.cn/blog-414166-562616.html)

Move fast and optimize gradually

## debug

Expose fault and transfer to failure

### assert()

### printf()

## static

code unused in other unit should be static

## RSRC rule

general reading src rule

### Tree

check whole structure

### Read from main

```bash
# find src of main
grep -i -n 'main\(.*\)' $(find . -iname '*.c') 2>/dev/null
find '*.c'| xargs grep -i -n 'main\(.*\)' --color 2>/dev/null
# fzf - an interactive dir/file finder
vim $(fzf)
# type main.c and enter into main.c

# find functiong in main.c
find -iname '*.c'| xargs  grep -i -n 'init_monitor\(.*\)' --color 2>/dev/null
vim $(fzf)
# type monitor.c
```

### macro

meta programming

Precompilation and expand macro

```bash
gcc -E ...
```

## git

### gitignore

```bash
# exclude everything in current dir
# cannot use dot as current dir
* 
# unexclude(or include) notebook subdir
!notebook/
```

## Reference

[vim-galore](https://github.com/mhinz/vim-galore)

[awesome-c](https://github.com/oz123/awesome-c)

[makefile tutorials](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/)

[visual-git-guide](https://marklodato.github.io/visual-git-guide/index-en.html)
