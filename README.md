# warhol

Colorize command output using grc and lscolors

## Installing

### [Zgen](https://github.com/tarjoilija/zgen)

Add `zgen load JayTheMarketer/warhol` to your .zshrc with your other load commands.

### [Antigen](https://github.com/zsh-users/antigen)

Add `antigen bundle JayTheMarketer/warhol` to your .zshrc

### [Oh-My-Zsh](http://ohmyz.sh/)

If you're using [oh-my-zsh](github.com/robbyrussell/oh-my-zsh):

1. Clone the repository into a new `warhol` directory in your custom plugins:

    ```zsh
    git clone https://github.com/unixorn/warhol $ZSH_CUSTOM/plugins/warhol
    ```

2. Edit your `~/.zshrc` and add `warhol` – same as clone directory – to the list of plugins to enable:

    ```zsh
    plugins=( ... warhol )
    ```

3. Then, restart your terminal application to **refresh context** and use the plugin. Alternatively, you can source your current shell configuration:

    ```zsh
    source ~/.zshrc
    ```

### Without using any frameworks

1. Clone the repository into a new `warhol` directory

    ```zsh
    git clone git@github.com:JayTheMarketer/warhol.git
    ```
2. Add its bin directory to your $PATH and source it in your `.zshrc` file.

    ```zsh
    echo "export PATH=/path/to/here/warhol:$PATH >> ~/.zshrc
    echo "source /path/to/here/warhol" >> ~/.zshrc
    ```

The scripts in here don't actually require you to be using ZSH as your login shell, they're being distributed as a [zgen](https://github.com/zsh-users/antigen) plugin because that's convenient.

## Tips

I've included the `LSCOLORS` and `LS_COLORS` settings from trapd00r's [LS_COLORS](https://github.com/trapd00r/LS_COLORS) in this plugin. I recommend installing the dircolors file located there to keep it updated. 

```bash
wget https://raw.github.com/trapd00r/LS_COLORS/master/LS_COLORS -O $HOME/.dircolors
```

Customizing `LSCOLORS` for OSX/*BSD and `LS_COLORS` for Linux is a hassle. It's even more of a hassle to keep them in sync across *BSD and Linux. 

Fortunately, Geoff Greer made an online tool that makes it easy to customize your color scheme and keep them in sync across Linux and OS X/*BSD available online at [lscolors](http://geoff.greer.fm/lscolors/). The easiest way to change the defaults is to redeclare the variable(s) in your `.zshrc` after your framework loads your plugins.

