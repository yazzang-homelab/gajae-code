### Fixed

- The bash tool guidance no longer tells the model that `nohup` / `setsid` / `disown` keep a daemon alive independent of the bash call. Since the shell guardian reaps every descendant of a retired worker, including new-session ones, a daemon detached inside an `async: true` job dies when the job's one-shot worker is retired; the guidance now says so and keeps the explicit large `timeout` as the way to run a long-lived daemon.
