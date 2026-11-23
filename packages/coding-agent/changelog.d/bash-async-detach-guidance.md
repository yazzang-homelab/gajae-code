### Fixed

- The bash tool guidance no longer tells the model that `nohup` / `setsid` / `disown` keep a daemon alive independent of the bash call. On POSIX, a managed bash call (foreground or `async: true`) runs on a one-shot shell worker whose owned descendants, including detached ones, are cleaned up when the call ends; the guidance now says so and directs long-running daemons to the foreground of an `async: true` call with an explicit `timeout`.
