
```
from pwn import *
context.arch = 'x64'

p = process("./file_name")
e = ELF("./file_name")
libc = ELF("libc.so.6')
r = ROP(e)

def slog(name, addr): return success(': '.join([name, hex(addr)]))

p.interactive()
```
