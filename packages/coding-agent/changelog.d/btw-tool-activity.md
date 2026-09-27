### Changed

- `/btw` side chats now include a `[main tool activity]` line on each assistant turn that called tools, listing each tool's name and reported outcome (`ok`, `error`, `pending`, or `unknown`) as of the moment the side chat opened. Tool arguments, intents, outputs, and details are still not sent to the side chat. Adjacent same-role turns in the side-chat scope are merged so strict-alternation providers accept the request.
