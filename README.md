# `pomo`

## Motivation

While following the [Learning How To Learn][1] on Coursera, the instructors
recommended the [Pomodoro Technique][2] to help overcome procrastination and
allow the brain to enter the "diffuse mode" of thinking, which is essential for
learning and problem-solving.

I wanted a simple pomodoro timer which would integrate well with the terminal,
as I got tired of setting alarms on my phone/desktop, and would often forget to
set them at all.

## Goals

1. As simple as possible
1. Minimal dependencies
1. Portable/POSIX conformant (or at least works on Mac & Linux)
1. Runs independently of the parent process (so if the terminal window is
   closed, the timer still runs, and is still able to alert the user)

[1]: https://www.coursera.org/learn/learning-how-to-learn/home/welcome
[2]: https://en.wikipedia.org/wiki/Pomodoro_Technique
