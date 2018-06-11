# Markdownc

A simple command line tool that takes markdown files and outputs html. This isn't much more than an alias of `pandoc` and markdown-css

## install

1. Install pandoc
   ```bash
   sudo apt install pandoc
   ```

1. Install the css themes
   ```bash
   cd $HOME/.local/share
   git clone https://github.com/otsaloma/markdown-css.git
   ```

1. Install this script
   ```bash
   mkdir $HOME/bin
   cd /tmp
   git clone <this repo>
   mv markdownc/markdownc $HOME/bin
   ```