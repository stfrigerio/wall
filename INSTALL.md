# Install

## Build

Needs Go ≥ 1.22.

```bash
git clone https://github.com/stfrigerio/wall
cd wall/go
go build -o wall .
```

## Put it on your `$PATH`

Most Linux systems already have a `wall` command (util-linux's, which
broadcasts a message to every terminal) in `/usr/bin`. Either install this one
under another name:

```bash
mkdir -p ~/.local/bin
ln -sf "$PWD/wall" ~/.local/bin/claude-wall
```

or keep the name `wall` and make sure `~/.local/bin` comes before `/usr/bin`
in your `$PATH`:

```bash
ln -sf "$PWD/wall" ~/.local/bin/wall
```

The link points at the binary in the repo, so after a `git pull` a rebuild
(`go build -o wall .`) is all an update takes.

## Uninstall

```bash
rm ~/.local/bin/claude-wall    # or ~/.local/bin/wall
```
