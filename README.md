from pwn import *

# libc = ELF("/lib/x86_64-linux-gnu/libc.so.6")
# libc = ELF("/lib/i386-linux-gnu/libc.so.6")

p = process("./rtl")
e = ELF("./rtl")


def slog(name, addr): return success(': '.join([name, hex(addr)]))

p.interactive()
