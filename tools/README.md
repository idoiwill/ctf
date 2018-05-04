# Tools experience in CTF
# Tools list
##Pwntools

set arch info

context(arch='x86_64',os='linux',endian='little')

set info/debug

context.log_level='debug'

set env of elf

    env = {'LD_PRELOAD':'/home/ctf/libc.so.6'}
    if DEBUG:
    	r = process('./xxx',env=env)
    else:
    	r = remote('202.120.7.210',1212)

debug program from exp

    print proc.pidof(p)
    raw_input('gdb attach')
