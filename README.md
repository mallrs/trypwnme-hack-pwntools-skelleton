
```
from pwn import *
# context.arch = 'amd64'
# context.log_level = 'debug'

p = process("./file_name")
e = ELF("./file_name")
libc = ELF("./libc.so.6')
r = ROP(e)

def slog(name, addr): return success(': '.join([name, hex(addr)]))

p.interactive()
```
