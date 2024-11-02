Course Code: https://theprimeagen.github.io/vim-fundamentals/
How File Works:  https://www.youtube.com/watch?v=VVdmmN0su6E

- `ed` is a line-oriented text editor. It is the standard text editor in Unix systems. It is a line editor, meaning that it can only operate on one line at a time. It is not a visual editor, so it does not display the text being edited. Instead, it uses a command-line interface to interact with the user. Use `q` and `Enter` to exit `ed`.

- `vimtutor` is a program that teaches you how to use Vim. It is a text-based tutorial that guides you through the basic commands and features of Vim. To start `vimtutor`, open a terminal and type `vimtutor` and press `Enter`. Follow the instructions on the screen to learn how to use Vim.

- Vim Game: https://vim-adventures.com/

**VIM**
- `:h usr<tab>`: Open the user manual in Vim.
- `:h usr<ctl-d>`: Show the next match.
- `<ctl-p>`: Go to the previous command.
- `<ctl-n>`: Go to the next command.
- `Ctrl-c`: Exit insert mode.
- `Ctrl-[`: Exit insert mode.
- `zz`: Center the cursor line on the screen.
- `dd`: Delete the current line.
- `shift + d`: Delete from the cursor to the end of the line.
- `7dd`: Delete 7 lines.
- `d$`: Delete from the cursor to the end of the line.
- `d0`: Delete from the cursor to the beginning of the line.
- `dgg`: Delete from the cursor to the beginning of the file.
- `dG`: Delete from the cursor to the end of the file.
- `d6j`: Delete 6 lines down.
- `d6k`: Delete 6 lines up.
- `u`: Undo the last change.
- `Shift-v + d`: Delete the current line.
- `yy`: Yank (copy) the current line.
- `p`: Paste the yanked text after the cursor.
- `P`: Paste the yanked text before the cursor.
- `v`: Enter visual mode to select text.
- `V`: Enter visual line mode to select lines.
- `V + y`: Yank the selected text.
- `V + d`: Delete the selected text.
- `:reg`: (register) Show the contents of the registers. Keeps track of the things you delete and yank.
- `i`: Insert text to the left of the cursor.
- `I`: Insert text at the beginning of the line.
- `a`: Append text to the right of the cursor.
- `A`: Append text at the end of the line.
- `o`: Open a new line below the current line.
- `O`: Open a new line above the current line.
- `s`: Substitute (delete and insert) the character under the cursor.
- `set number`: Show line numbers.
- `set nonumber`: Hide line numbers.
- `set scrolloff=5`: Keep a minimum of 5 lines above and below the cursor.
- `set relativenumber` or `set rnu`: Show relative line numbers.
- `colorscheme <color>`: Change the color scheme.


> add commands in .vimrc to readme as well
> add commands on apple notes to readme as well

- `vim .`: Open the current directory in Vim.
- `j` or `k`: Move the cursor down or up.
- `h` or `l`: Move the cursor left or right.
- `Enter`: Navigate the the folder or open the file.
- `Ex`: Close the file and go back to the file explorer.
- `Vex`: Vertical split the file explorer.
- `Sex`: Horizontal split the file explorer.
- `<Ctrl-w>`: Enter window mode.
- `<Ctrl-w> + s`: Split the window horizontally.
- `<Ctrl-w> + v`: Split the window vertically.
- `<Ctrl-w> + w`: Switch between windows.
- `<Ctrl-w> + q`: Close the current window.
- `<Ctrl-w> + h`: Move to the window on the left.
- `<Ctrl-w> + j`: Move to the window below.
- `<Ctrl-w> + k`: Move to the window above.
- `<Ctrl-w> + l`: Move to the window on the right.
- `<Ctrl-w> + o`: Close all windows except the current one.
- 
    `n`: mode (normal), i - insert, v - visual, c - command, t - terminal
    `nore`: no remap
    `map <leader>pv :Vex<CR>`: map leader + pv to open the file explorer in a vertical split (:Vex + Enter)
- `imap xx yy`: map xx to yy in insert mode.
- `so: %`: Source the current file.
- `:e <file-name>`: Edit the file.
- `:e **/*/<file-name> <tab>`: Edit the file in the current directory and subdirectories.
- `m  shift + <letter>`: Mark the current position (Global level mark).
- `m <letter>`: Mark the current position (Local/Buffer level mark).
- `' shift + <letter>`: Go to the marked position.
- `' <letter>`: Go to the marked position.
- `ctrl + ^` or `ctrl + 6`: Go to the previous file.
- `ctrl + o`: Go to the previous location or movement.
- `ctrl + i`: Go to the next location or movement.

plugin manager: https://github.com/junegunn/vim-plug
fuzzy finder: https://github.com/junegunn/fzf.vim
```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
- `:PlugInstall`: Install the plugins.
- `:PlugUpdate`: Update the plugins.
- `:Files`: Fuzzy find files.
- `:GFiles`: Fuzzy find files in the git repository.
- `ctrl + p`: Go to the previous file.
- `ctrl + n`: Go to the next file.

Quickfix list
Ripgrep: https://github.com/BurntSushi/ripgrep?tab=readme-ov-file#installation
- (Using Ripgrep plugin) `:Rg <pattern>` (:Rg SOCKET): Search for the pattern in the files. `<tab>`: to select multiple files in fzf. If pressed `<CR>` or enter, you will get into quickfix list
- (Using vim grep): `:grep <word-pattern> <file-pattern>` (:grep SOCKET **/*.c): Searching for pattern in the files. press enter to navigate into the file or press `!` to silence it. `:copen` to go to search results (quickfix list). `:cnext` will move to the next one, `:cprev` will move to the previous one. c stands for quick. `:cdo` to execute a command accross all of your quick fix list. `:wa` to write all the fixes and save.

Search and Replace
- `:set noic`: Turn off ignore case.
- `/<word>`: Search for the word. `n` to go to the next match, `N` to go to the previous match.
- `:set hls ic`: Highlight search and ignore case.
Regex Licensing: https://regexlicensing.org/citation/
- `:nohls`: Turn off the highlight search.
- `:s/<word>/<replacement>`: Replace the word with the replacement for the current line.
- `:%s/<word>/<replacement>`: Replace the word with the replacement for the entire file.
- `:'<,'>s/<word>/<replacement>`: Replace the word with the replacement for the selected lines (visual line). You can select multiple line by pressing `shift + v` and then `j` or `k` to select the lines.
- `:s/<word>/<replacement>/g`: Replace all occurrences of the word with the replacement for the current line.
- `:s/<word>/<replacement>/gc`: Replace all occurrences of the word with the replacement for the current line with confirmation.
- `:'<,'>s/(\(.*\) && \(.*\))/(\2 \&\& \1)`

Macros
- `q<letter>`: Start recording a macro.
- `q`: Stop recording a macro.
- `@<letter>`: Play the macro.
- `@@`: Play the last played macro.
- `10@<letter>`: Play the macro 10 times.
- `:reg`: Show the contents of the registers.
- `:reg a`: Show the contents of the register a.
- `_`: The cursor will got the the first non-blank character of the line.
- `:ctrl + a`: Increment the number under the cursor.
- `:ctrl + x`: Decrement the number under the cursor.
ex. `q a V yy p C-a q`: Record a macro to duplicate the line and increment the number. `@a` to play the macro.
- `dt<character>`: Delete until the character.
- `df<character>`: Delete until and including the character.
- `dT<character>`: Delete backward until the character.
- `dF<character>`: Delete backward until and including the character.
- `di<character>`: Delete inside the character. `o` to go to the other end of the character. `diw` to delete the word. `diW` to delete the non-whitespace word(from non-white space to non-white space).
- `da<character>`: Delete around the character.
- `ci<character>`: Change inside the character. (Delete and insert)
- `ca<character>`: Change around the character.
- `vi<character>`: Select inside the character.
- `va<character>`: Select around the character.
- `yi<character>`: Yank inside the character.
- `ya<character>`: Yank around the character.
- `d$`: Delete from the cursor to the end of the line.
- `d0`: Delete from the cursor to the beginning of the line.
- `dgg`: Delete from the cursor to the beginning of the file.
- `dG`: Delete from the cursor to the end of the file.
- `f<character>`: Find the character.
- `F<character>`: Find the character backward.
- `"ay`: Yank the selected text to register a.
- `"ap`: Paste the text from register a.

advanced motion
- `_`: Go to the first non-blank character of the line.
- `g_`: Go to the last non-blank character of the line.
- `0` or `^`: Go to the beginning of the line.
- `$`: Go to the end of the line.
- `D` or `d$`: Delete from the cursor to the end of the line.
- `C` or `c$`: Change from the cursor to the end of the line.
- `S`: Delete the current line respecting the indentation and enter insert mode.
- `x`: Delete the character under the cursor.
- `X`: Delete the character before the cursor.
- `s`: Substitute (delete and insert) the character under the cursor.
- `f<character>`: Find the character. `;` to go to the next match, `,` to go to the previous match. 
- `F<character>` to find the character backward. `,` to go to the next match, `;` to go to the previous match.
- `t<character>`: Till the character. `;` to go to the next match, `,` to go to the previous match. 
- `T<character>` to find the character backward. `,` to go to the next match, `;` to go to the previous match.
- `}`: Go to the next paragraph.
- `{`: Go to the previous paragraph.
- `(`: Go to the previous sentence.
- `)`: Go to the next sentence.
- `[[`: Go to the previous section.
- `]]`: Go to the next section.
- `C + d`: Scroll down half a page.
- `C + u`: Scroll up half a page.
- `%`: Go to the matching parenthesis, bracket, or brace.

Cool remaps
- `vnoremap <leader>p "_dp`: Paste without yanking the text.
- `vnoremap <leader>y "+y`: Copy to the system clipboard.
- `nnoremap <leader>y "+y`: Copy to the system clipboard.
- `nnoremap <leader>Y gg"+yG`: Copy the entire file to the system clipboard.
- `vnoremap J :m '>+1<CR>gv=gv`: Move the selected lines down.
- `vnoremap K :m '<-2<CR>gv=gv`: Move the selected lines up.

Create a new file and plugins
- `%` in file explorer to create a new file. `D` to delete the file and `R` to rename the file.
https://vimways.org/2019/writing-vim-plugin/
https://github.com/tpope
https://vimways.org/2019/writing-vim-plugin/
https://github.com/tpope/vim-fugitive