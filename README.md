# `pomo`

A very simple [pomodoro][1] timer, which runs independently of the shell from
which it's called, so you don't have to keep the terminal window open to
receive the alert.

It detects what terminal/multiplexer you are using and opens the alert
screen via the same application, so alerts are consistent yet flexible.

## Goals

1. As simple as possible
1. Minimal dependencies
1. Doesn't rely on a particular shell syntax (thus POSIX syntax)
1. Doesn't rely on a particular desktop environment or Linux distribution
   (Ideally will also work on OS X)
1. Runs independently of the parent process (so if the terminal window is
   closed, the timer still runs, and is still able to alert the user)

## Dependencies

* POSIX utilities: `[` `kill` `printf` `ps` `read` `rm` `sleep` `stty`
* `tmux` (recommended) *or* `screen`, *or* some kind of terminal emulator
   which supports the `-e <command>` option.

## TODO:

- [ ] OS X testing (Terminal and iTerm2)

## Example usage:

![Pomo example usage and alert demo with GNU screen](./media/pomo_ex-1.gif)

## Install

Should work fine in any POSIX compliant shell.

```shell
# `foo` is a directory in your `$PATH`
cd foo

# Download the raw script file
curl -so ./pomo https://raw.githubusercontent.com/jaf7C7/pomo/master/pomo 

# Make the script executable
chmod +x pomo
```

Or alternatively if you want the entire repo:

```shell
# Clone the repository
git clone https://github.com/jaf7C7/pomo

# Enter the repository
cd pomo

# Make the script executable
chmod +x pomo

# Create a symlink to the executable in a directory `foo` in your `$PATH`
ln -s pomo foo/pomo

```

[1]: https://en.wikipedia.org/wiki/Pomodoro_Technique
