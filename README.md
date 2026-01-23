This is my personal gentoo low bloat kernel config.
It's specific to my hardware: AMD CPU/GPU and my ASUS motherboard.
Don't expect it to work for you.

Latest commit:
- Changed Transparent Hugepage to MADVISE (always was causing overhead when reorganising memory)
- Enabled BBR congestion control and set it as default
- Enabled MAGIC_SYSRQ (not sure why I had it disabled)
- Added IKCONFIG (lightweight and useful)
- Changed ZRAM backend compression from LZ4 to ZSTD as its got better compression for modern ryzen systems.
- Enabled compression for the limited NTFS RW support
