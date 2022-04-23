# Dev Notes

## My Commandline Tooling

- shell is zsh with [omz](https://ohmyz.sh/)
- with autosuggestions and syntaxhighlighting [instructions](https://dev.to/kumareth/a-beginner-s-guide-for-setting-up-autocomplete-on-ohmyzsh-hyper-with-plugins-themes-47f2)

- [`fzf`](https://github.com/junegunn/fzf) - fuzzy finder, most useful with `ctrl-R`-Keybinding for interactive cmd-history search
- [`z`](https://github.com/rupa/z/) - For Jumping to frequently used directories with fuzzy search e.g `z shared`
- [`tldr`](https://tldr.sh/) - usage examples for frequent commands. e.g. `tldr ssh`
- [`fkill`](https://github.com/sindresorhus/fkill-cli) - interactively kill processes by name, pid or port e.g. `fkill firefox`
- [git-delta](https://crates.io/crates/git-delta) - improves `git diff` and `git show`
- [`ncdu`](https://dev.yorhel.nl/ncdu) - analyze diskusage with friendly ui
- [`bat`](https://github.com/sharkdp/bat) - more beautiful `cat` output
- [`wl-copy`](https://github.com/bugaevc/wl-clipboard) - copy anything from the commandline e.g. `cat .ssh/id_rsa.pub | wl-copy`

## Commandline Tricks

**shortcuts**
- `ctrl`-`l` clear terminal
- `ctrl`-`u` clear line
- `ctrl`-`z` "minimize" current program (`fg` to bring it back)
- `ctrl`-`a` jump to line start
- `ctrl`-`e` jump to line end
- `ctrl`-`w` delete last word

**commands**
- `sudo !!` - run the last command with sudo
- `tail -f` - follow the newest lines of a file
- `column -t` - text to an aligned table e.g.: `mount | column -t`
- `jq` - prettify json e.g.: `nc -l -p 8080 | jq`

## SSH Tricks

- `users` / `who` / `w` - find out which users are currently logged in.
- [`byobu`](https://www.byobu.org/) - teminal-based window manager. Keep your sessions between ssh-logins.
- `tmux new-session -s sessionname` + `tmux attach-session -t sessionname` - Share your terminal-session with multiple users (see `tldr tmux`, [tmux-command](https://github.com/tmux/tmux), [tutorial](https://www.howtoforge.com/sharing-terminal-sessions-with-tmux-and-screen))

## Some Favourite Python libraries

- [FastAPI](https://fastapi.tiangolo.com/) - Web-api fast.
- [Typer](https://typer.tiangolo.com/) - easy CLI
- [tqdm](https://github.com/tqdm/tqdm) - easy progressbar with pandas-support

## On Gunicorn, Uvicorn and Fastapi in Production

**In a Kubernetes Cluster** deployment is recommended to be done via custom container from the python base image.

Load balancing and replication should be handled at the cluster level.

```Dockerfile
FROM python:3.10.0-slim

WORKDIR app

COPY <requirements>
RUN <install dependencies>

COPY <code directory> ./<code directory>

CMD uvicorn app.main:app --host 0.0.0.0

```

source: [Fastapi Docs](https://fastapi.tiangolo.com/deployment/docker/)

**Without a cluster** you should check out the [uvicorn deployment documentation](https://www.uvicorn.org/deployment/).