### Changed

- `/btw` side chats now see which tools the main session called and whether each call succeeded, failed, or is still pending, as `[main tool activity]` lines on the owning assistant turn. Tool arguments, intents, outputs, details, and file contents still never enter the side-chat scope, so a mid-task question no longer sees only the user's own messages.
