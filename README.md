This is my personal gentoo low bloat kernel config.
It's specific to my hardware: AMD CPU/GPU and my ASUS motherboard.
Don't expect it to work for you.

24/Jan commit:
- Changed Transparent Hugepage to MADVISE (always was causing overhead when reorganising memory)
- Enabled BBR congestion control and set it as default
- Enabled MAGIC_SYSRQ (not sure why I had it disabled)
- Added IKCONFIG (lightweight and useful)
- Changed ZRAM backend compression from LZ4 to ZSTD as its got better compression for modern ryzen systems.
- Enabled compression for the limited NTFS RW support

27/Jan commit:
- Disable function tracing but maintain support for profiling (needed for jit)
- Switch to LTO FULL
- Disable kprobes and events
- Disable KALLSYMS ( i personally never need it, but can easily re-enable if I do)
