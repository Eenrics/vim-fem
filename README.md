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