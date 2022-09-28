# nvim-startup

## Setting up:

```sh
cd $HOME
git init
git remote add origin https://github.com/tyarn/nvim-startup
git pull origin main
```

This will put all the files from this repo in your home directory. You are then
free to `rm -rf .git` to remove the git history and re-initialize to your own
repository as you see fit.

## Installing neovim

After performing the clone above, ensure that `~/.local/bin` is on your `PATH`
variable. If it's not, add this line to your `~/.bashrc`:

```sh
export PATH="$HOME/.local/bin:$PATH"
```

just pass in a neovim version to the `install-nvim` command:

```sh
install-nvim "0.7.0"
```

The installation script for `nvim` is included at `.local/bin/install-nvim`.
It will place the `nvim` executable in `~/.local/bin`, so ensure that
`~/.local/bin/nvim` appears before other installations on your `PATH`.

## Swapping color schemes
# Installing a new color scheme
Once you find a color scheme you like you can automatically install it (next time you open nvim) by editing `.config/nvim/init.vim` and searching for the term "Coloring", you should see a bunch of lines that look like `Plug 'romainl/Apprentice'`
Once you are here you just need to find a color scheme you like by looking them up, but a good reference is here: https://vimcolorschemes.com/
Once you find one you like, you take the git repo it points to and add it as a plugin
For example
If I wanted to install this color scheme here: https://github.com/wadackel/vim-dogrun
I would add the line `Plug 'wadackel/vim-dogrun` to the plugins section for coloring
See the next section for how to set your new color

# Setting a new color
If you want to swap your installed color you can do that by editing the file `.config/nvim/init.vim`
Search for the line with `Color theme` (it should be commented out, any line that starts with a " is a comment)
If you want to add the color `vim-dogrun` as the color to use, comment out the uncommented line that starts with `colo`
and write the line 
`colo vim-dogrun` 
Restart nvim to see your new color!
