# ys

## How it works
ys uses a hybrid approach for maximum precision with minimal CPU overhead:
- **Sleep phase** — for waits longer than 20ms, it delegates most of the time to AHK's `Sleep` command (low CPU usage)
- **Busy-wait phase** — the final ~20ms spins on `QueryPerformanceCounter` for sub-millisecond accuracy

## Usage
```autohotkey
#Include ySleep.ahk

; Sleep for exactly 100ms
ySleep(100)
```

## Installation
Drop `ySleep.ahk` into your project and `#Include` it.
