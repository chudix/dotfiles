# Read Me

## Structure

[init.el](./init.el): This is the main configuration file wich set up
global settings and import each config module.

[settings](./settings): This directory contains all modules.

## init.el

As said it contains the main configurations and links the modularized
config scripts.

It uses a subdirectory( */settings* ) that should live under
*$HOME/.emacs.d/*.

Simply link all files under this directory to *~/.emacs.d/settings* and it should work.

``` shell
ln {<path_to_dotfiles>,$HOME/.emacs.d}/init.els
```

``` shell
mkdir $HOME/.emacs.d/settings
```

``` shell
for filename in $(ls <path_to_dotfiles>/emacs/settings)
do
ln -s $HOME/{<path_to_dotfiles>/emacs/,.emacs.d/}settings/$filename 
done

```

## Settings directory

Contains three config files at the moment.

  * [appearance.el][./appearance.el]: Has configuration regarding
  visualization of emacs.

  * [behaviour.el][./behaviour.el]: Holds configurations regarding how
  emacs works when editing. Such as: tab width and other stuff
  
  * [plugins.el][./plugins.el]: Holds plugins initialization. Uses the use-package macro.
  
  * [keybindings.el][./keybindings.el]: Holds some keybindings


[./appearance.el]: ./appearance.el "appearance"

[./behaviour.el]: ./behaviour.el "behaviour"

[./plugins.el]: ./plugins.el "plugins"

[./keybindings.el]: ./keybindings.el "keybindings"
