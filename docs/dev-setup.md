# Dev-Tools

## Commandline Tooling

- [`fzf`](https://github.com/junegunn/fzf) - fuzzy finder, most useful with `ctrl-R`-Keybinding for interactive cmd-history search
- [`z`](https://github.com/rupa/z/) - For Jumping to frequently used directories with fuzzy search e.g `z shared`
- [`tldr`](https://tldr.sh/) - usage examples for frequent commands. e.g. `tldr ssh`
- [`fkill`](https://github.com/sindresorhus/fkill-cli) - interactively kill processes by name, pid or port e.g. `fkill firefox`
- [git-delta](https://crates.io/crates/git-delta) - improves `git diff` and `git show`
- [`ncdu`](https://dev.yorhel.nl/ncdu) - analyze diskusage with friendly ui

### On a Remote Machine

- `users` / `who` / `w` - find out which users are currently logged in.
- [`byobu`](https://www.byobu.org/) - teminal-based window manager. Keep your sessions between ssh-logins.
- `tmux new-session -s sessionname` + `tmux attach-session -t sessionname` - Share your terminal-session with multiple users (see `tldr tmux`, [tmux-command](https://github.com/tmux/tmux), [tutorial](https://www.howtoforge.com/sharing-terminal-sessions-with-tmux-and-screen))

## Python libraries

- [FastAPI](https://fastapi.tiangolo.com/) - Web-api fast.
- [Typer](https://typer.tiangolo.com/) - easy CLI
- [tqdm](https://github.com/tqdm/tqdm) - easy progressbar with pandas-support
