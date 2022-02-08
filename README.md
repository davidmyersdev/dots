# dots

Manage your dotfiles with ease, and pair with a parter if you want to.

## Installation

```bash
dots [-fhl] <profile>

  -f  Force removal of existing files in \$HOME directory
  -h  Show usage/help info
  -l  List available (and current) profile(s)
  -p  Purge links from any active profile
```

To get started, download this project.

```bash
git clone https://github.com/voraciousdev/dots && cd dots
```

Next, clone your dotfiles into the `profiles` directory. It helps to give the project an alias too, because profiles are named from the directory.

```bash
git clone https://github.com/voraciousdev/dotfiles ./profiles/david
```

## Usage

You can sync your dotfiles to `$HOME` with the `dots` command.

```bash
./bin/dots david
```

To list available profiles, use the `-l` flag. An active profile will be labeled as `current` in the list.

```bash
$ dots -l

Available profiles:
 - david (current)
```

## Extras

### Use it Anywhere

To use it from anywhere, you need to symlink the file into your `PATH`.

```bash
# assumptions:
# - you are in the dots git directory
# - you have /usr/local/bin added to your PATH
ln -s $(pwd)/bin/dots /usr/local/bin/dots
```
