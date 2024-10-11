# Markdownc

A simple command line tool that takes markdown files and outputs html. This isn't much more than a wrapper of `pandoc` and [markdown-css](https://github.com/otsaloma/markdown-css)

## Install

1. Install pandoc and inotify-tools
   ```bash
   sudo apt install pandoc inotify-tools
   ```

1. Install the css themes
   ```bash
   cd $HOME/.local/share
   git clone git@github.com:murphym18/markdown-css.git
   ```

1. Install this script
   ```bash
   mkdir -p $HOME/.local/bin
   cd /tmp
   git clone https://github.com/murphym18/markdownc.git
   cd markdownc
   cp markdownc markdownc-watch markdown-spellcheck ~/.local/bin/
   ```

## Usage

Give markdownc the markdown file you wish to turn into html. Here is an example 

```bash
markdownc foo.md
```

With this input, the program will create `foo.html` 

## Extras

There are two other helper programs:

- markdownc-watch
- markdownc-http

`markdownc-watch` will auto-run `markdownc` whenever you save changes to your file. To use it:
```bash
markdownc-watch foo.md
```

`markdownc-http` will also auto-run `markdownc` when you save changes, but it will run an HTTP server too. The HTTP server will live-reload when you make changes. To use this you need to isntall `browser-sync` like so:
```bash
npm install -g browser-sync
```

Then to use the `markdownc-http` run:
```bash
markdownc-http foo.md
```

This will compile `foo.md` to `foo.html`, start `markdownc-watch`, and start `browser-sync`. You can then open http://localhost:3000/foo.html to see a live preview of your markdown rendered to HTML.

