# relay-doorbell

A content-free signal board for a two-person mentor relay.

This repo holds **only two counter files** — no messages, no personal data,
nothing else, ever:

- `to-mentor.txt` — bumped by the mentee's side when it files a relay
  message (or rings manually). The mentor's agent polls this file and
  wakes for a relay check when the value changes.
- `to-mentee.txt` — bumped by the mentor's side when it files a relay
  message (or rings manually). The mentee's agent polls this file the
  same way.

A "bump" = replacing the file's contents with the current UTC timestamp.
The value itself means nothing; only the change matters. All real
communication lives in the private relay repo — this board is just a
doorbell.
