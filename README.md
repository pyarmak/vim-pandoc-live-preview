# A Vim Plugin for Lively Previewing pandoc PDF Output

This plugin provides a live preview of the output PDF of your file using pandoc. The
display of the output PDF file will be updated lively as you type (just hold
the cursor and you will see the PDF file updated). Currently,
vim-pandoc-live-preview only support UNIX-like systems. Please let me know if
you have any suggestions.

## Installation

Before installation, you need to make sure your Vim version is later than 7.3,
and is compiled with `+python` feature. Then copy `plugin/pandoclivepreview.vim`
to `~/.vim/plugin`.

By default, you need to have [evince][] or [okular][] installed as pdf viewers.
But you can specify your own viewer by setting `g:livepreview_previewer`
option in your `.vimrc`:

    let g:livepreview_previewer = 'your_viewer'

Please note that not every pdf viewer could work with this plugin. Currently
evince and okular are known to work well. You can find a list of known working
pdf viewers [here](https://github.com/xuhdev/vim-latex-live-preview/wiki/Known-Working-PDF-Viewers).

## Usage

Simply execute `:LLPStartPreview` to launch the previewer. Then try to type in
Vim and you should see the live update. The updating time could be set by Vim's
['updatetime'][] option. If your pdf viewer crashes when updates happen, you can
try to set 'updatetime' to a higher value to make it update less frequently. The
suggested value of 'updatetime' is `1000`.

## Screenshot


<!--
The screenshot is at ./screenshots/
-->

['updatetime']: http://vimdoc.sourceforge.net/htmldoc/options.html#%27updatetime%27
[evince]: http://projects.gnome.org/evince/
[okular]: http://okular.kde.org/
