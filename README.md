# VIM-GRADLE #

This vim bundle simply recognizes .gradle files as being groovy syntax.  It also adds a vim compiler
plugin for gradle.

## Installation ##

### pathogen
- Install [pathogen](http://www.vim.org/scripts/script.php?script_id=2332) into `~/.vim/autoload/` and add the
   following line to your `~/.vimrc`:

        call pathogen#infect()

- Make a clone of the `vim-gradle` repository:

        mkdir -p ~/.vim/bundle
        cd ~/.vim/bundle
        git clone https://github.com/tfnico/vim-gradle

- OR use git submodules:

        git submodule add https://github.com/tfnico/vim-gradle.git bundle/vim-gradle
        git submodule init

Of course, if you use [Janus](https://github.com/carlhuda/janus/), you should put the clone in ~/.janus/
instead.

That's it. Pathogen should handle the rest.

### vim-plug

add following line to your `~/.vimrc`, or `~/.config/nvim/init.vim` if you use neovim:

    Plug 'QiBaobin/vim-gradle'

## Usage ##

### Syntax Highlighting ###

.gradle files will now have groovy syntax highlighting.

### Compiler Plugin ###

You can now use `:compiler gradle` to set gradle as the compiler. `:make build` will then run
`gradle build` (for example) and the quickfix window will be loaded with parsed error results.


### Different gradle distribution

You can use below line to set a different a different distribution, like gradlew:

    set makeprg=./gradlew

## Credits ##

Inspiration from [vim-less](https://github.com/groenewege/vim-less).
