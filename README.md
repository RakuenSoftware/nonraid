# nonraid

Standalone nonRaid array implementation for SmoothNAS.

nonRaid models the Unraid-style storage layout: each data disk owns an
individual filesystem, and one to three parity disks protect those data disks.
Data disks may be different sizes, but no data disk can exceed the smallest
parity disk.

This module contains the portable layout validator, parity engine, Galois-field
math, and Linux NBD transport. SmoothNAS owns the appliance-specific control
plane, DB rows, API handlers, and mount orchestration.
