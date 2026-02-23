# TTP — Taskfile Transfer Protocol

TTP (Taskfile Transfer Protocol) is a minimalist binary protocol designed exclusively for communication between clients and the application server of a taskfile running over TCP.

- It is not a generic protocol.

It exists to transport operations on tasks with:
- Minimal overhead
- Trivial parsing
- High concurrency
- Low latency

Append-only persistence

The minimum required per frame is 35 bytes.

```

Initial protocol identification     (5 bytes)

Task GUID                           (16 bytes)

Task description size               (2 bytes)

Project name size                   (1 byte)

Author name size                    (1 byte)

Creation Timestamp                  (8 bytes)

Priority                            (1 byte) -> H, M, L

End                                 (1 byte) -> 20
```


