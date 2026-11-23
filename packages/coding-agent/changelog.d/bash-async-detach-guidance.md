### Fixed

- The bash tool guidance no longer tells the model that `nohup` / `setsid` / `disown` keep a daemon alive independent of the bash call. On POSIX, the one-shot worker for a managed non-PTY bash shell job, foreground or `async: true`, is retired when command execution ends, and its owned descendants, including detached ones, are cleaned up during retirement; the guidance now says so and directs long-running daemons to the foreground of an `async: true` call with an explicit `timeout`.
