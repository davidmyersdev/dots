# pairable

A dotfiles manager for smoother pairing.

## Usage

Usage is pretty simple:

```shell
# help
pairable [-fhl] <profile>
  -f  force removal of existing files in $HOME directory
  -h  show usage/help info
  -l  list available (and current) profile(s)
```

To get started, just download your and your pair's dotfiles into the `profiles` directory.

```shell
# it helps to alias your dotfiles
git clone https://github.com/drm2/dotfiles drm2
```

Profiles are named based on the directory name under `profiles`

```shell
# using the drm2 profile from the example above
pairable drm2
```

To list available profiles, just use the `-l` flag. If one of the available profiles is already active, it will be labeled as such.

```shell
# input
pairable -l

# output
Available profiles:
 - drm2 (current)
 - other
```

## Extras

### Use it Anywhere

To use it from anywhere, you just need to symlink the file into your `PATH`.

```shell
# assumptions:
# - you are in the pairable git directory
# - you have /usr/local/bin added to your PATH
ln -s $(pwd)/bin/pairable /usr/local/bin/pairable
```
