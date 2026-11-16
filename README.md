# IOKit

The IOKit side that Mac programs and daemons talk to, in user space.  (The kernel half, the registry nodes `io_nodes` served over Mach IPC — IOSurfaceRoot, IONameMatch, `io_registry_entry_get_property_bin_buf` — lives in `darwinator`: `src/mach_ipc.c`.)

- `hid-stub/` — `hid-stub`, a stand-in for `com.apple.iohideventsystem`: takes the service from launchd, answers the open with a port and everything else with success; for finding out what a client of the HID event system sends, and as the base of the real replacement.

To do: the registry data as files (display, power, backlight), HID events from the window server (`WindowServer`) to the Mac clients.

## Upstream sources (starting point)
`upstream/` holds unmodified source of other open projects (see [PROVENANCE.md](PROVENANCE.md)).  Survey: https://github.com/pearOS-bsd/docs/blob/main/development/EXISTING-PROJECTS.md
