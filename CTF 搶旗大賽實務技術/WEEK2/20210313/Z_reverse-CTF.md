#
```
https://zh-tw.facebook.com/455550404836569/videos/988158315026365/

https://github.com/ss8651twtw/Reverse-CTF-writeups
```
```
http://reversing.kr/

https://pwnable.tw/
```
# 1.Reverse-50
```
file reverse
chmod +x reverse
./reverse
strings reverse

readelf -a reverse
```
```
 readelf -a reverse
ELF Header:
  Magic:   7f 45 4c 46 01 01 01 00 00 00 00 00 00 00 00 00 
  Class:                             ELF32
  Data:                              2's complement, little endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - System V
  ABI Version:                       0
  Type:                              EXEC (Executable file)
  Machine:                           Intel 80386
  Version:                           0x1
  Entry point address:               0x8048340
  Start of program headers:          52 (bytes into file)
  Start of section headers:          6140 (bytes into file)
  Flags:                             0x0
  Size of this header:               52 (bytes)
  Size of program headers:           32 (bytes)
  Number of program headers:         9
  Size of section headers:           40 (bytes)
  Number of section headers:         31
  Section header string table index: 28

Section Headers:
  [Nr] Name              Type            Addr     Off    Size   ES Flg Lk Inf Al
  [ 0]                   NULL            00000000 000000 000000 00      0   0  0
  [ 1] .interp           PROGBITS        08048154 000154 000013 00   A  0   0  1
  [ 2] .note.ABI-tag     NOTE            08048168 000168 000020 00   A  0   0  4
  [ 3] .note.gnu.build-i NOTE            08048188 000188 000024 00   A  0   0  4
  [ 4] .gnu.hash         GNU_HASH        080481ac 0001ac 000020 04   A  5   0  4
  [ 5] .dynsym           DYNSYM          080481cc 0001cc 000060 10   A  6   1  4
  [ 6] .dynstr           STRTAB          0804822c 00022c 00004f 00   A  0   0  1
  [ 7] .gnu.version      VERSYM          0804827c 00027c 00000c 02   A  5   0  2
  [ 8] .gnu.version_r    VERNEED         08048288 000288 000020 00   A  6   1  4
  [ 9] .rel.dyn          REL             080482a8 0002a8 000008 08   A  5   0  4
  [10] .rel.plt          REL             080482b0 0002b0 000018 08  AI  5  24  4
  [11] .init             PROGBITS        080482c8 0002c8 000023 00  AX  0   0  4
  [12] .plt              PROGBITS        080482f0 0002f0 000040 04  AX  0   0 16
  [13] .plt.got          PROGBITS        08048330 000330 000008 00  AX  0   0  8
  [14] .text             PROGBITS        08048340 000340 0001c2 00  AX  0   0 16
  [15] .fini             PROGBITS        08048504 000504 000014 00  AX  0   0  4
  [16] .rodata           PROGBITS        08048518 000518 000035 00   A  0   0  4
  [17] .eh_frame_hdr     PROGBITS        08048550 000550 00002c 00   A  0   0  4
  [18] .eh_frame         PROGBITS        0804857c 00057c 0000cc 00   A  0   0  4
  [19] .init_array       INIT_ARRAY      08049f08 000f08 000004 00  WA  0   0  4
  [20] .fini_array       FINI_ARRAY      08049f0c 000f0c 000004 00  WA  0   0  4
  [21] .jcr              PROGBITS        08049f10 000f10 000004 00  WA  0   0  4
  [22] .dynamic          DYNAMIC         08049f14 000f14 0000e8 08  WA  6   0  4
  [23] .got              PROGBITS        08049ffc 000ffc 000004 04  WA  0   0  4
  [24] .got.plt          PROGBITS        0804a000 001000 000018 04  WA  0   0  4
  [25] .data             PROGBITS        0804a018 001018 000008 00  WA  0   0  4
  [26] .bss              NOBITS          0804a020 001020 000004 00  WA  0   0  1
  [27] .comment          PROGBITS        00000000 001020 000034 01  MS  0   0  1
  [28] .shstrtab         STRTAB          00000000 0016f0 00010a 00      0   0  1
  [29] .symtab           SYMTAB          00000000 001054 000460 10     30  47  4
  [30] .strtab           STRTAB          00000000 0014b4 00023c 00      0   0  1
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings)
  I (info), L (link order), G (group), T (TLS), E (exclude), x (unknown)
  O (extra OS processing required) o (OS specific), p (processor specific)

There are no section groups in this file.

Program Headers:
  Type           Offset   VirtAddr   PhysAddr   FileSiz MemSiz  Flg Align
  PHDR           0x000034 0x08048034 0x08048034 0x00120 0x00120 R E 0x4
  INTERP         0x000154 0x08048154 0x08048154 0x00013 0x00013 R   0x1
      [Requesting program interpreter: /lib/ld-linux.so.2]
  LOAD           0x000000 0x08048000 0x08048000 0x00648 0x00648 R E 0x1000
  LOAD           0x000f08 0x08049f08 0x08049f08 0x00118 0x0011c RW  0x1000
  DYNAMIC        0x000f14 0x08049f14 0x08049f14 0x000e8 0x000e8 RW  0x4
  NOTE           0x000168 0x08048168 0x08048168 0x00044 0x00044 R   0x4
  GNU_EH_FRAME   0x000550 0x08048550 0x08048550 0x0002c 0x0002c R   0x4
  GNU_STACK      0x000000 0x00000000 0x00000000 0x00000 0x00000 RW  0x10
  GNU_RELRO      0x000f08 0x08049f08 0x08049f08 0x000f8 0x000f8 R   0x1

 Section to Segment mapping:
  Segment Sections...
   00     
   01     .interp 
   02     .interp .note.ABI-tag .note.gnu.build-id .gnu.hash .dynsym .dynstr .gnu.version .gnu.version_r .rel.dyn .rel.plt .init .plt .plt.got .text .fini .rodata .eh_frame_hdr .eh_frame 
   03     .init_array .fini_array .jcr .dynamic .got .got.plt .data .bss 
   04     .dynamic 
   05     .note.ABI-tag .note.gnu.build-id 
   06     .eh_frame_hdr 
   07     
   08     .init_array .fini_array .jcr .dynamic .got 

Dynamic section at offset 0xf14 contains 24 entries:
  Tag        Type                         Name/Value
 0x00000001 (NEEDED)                     Shared library: [libc.so.6]
 0x0000000c (INIT)                       0x80482c8
 0x0000000d (FINI)                       0x8048504
 0x00000019 (INIT_ARRAY)                 0x8049f08
 0x0000001b (INIT_ARRAYSZ)               4 (bytes)
 0x0000001a (FINI_ARRAY)                 0x8049f0c
 0x0000001c (FINI_ARRAYSZ)               4 (bytes)
 0x6ffffef5 (GNU_HASH)                   0x80481ac
 0x00000005 (STRTAB)                     0x804822c
 0x00000006 (SYMTAB)                     0x80481cc
 0x0000000a (STRSZ)                      79 (bytes)
 0x0000000b (SYMENT)                     16 (bytes)
 0x00000015 (DEBUG)                      0x0
 0x00000003 (PLTGOT)                     0x804a000
 0x00000002 (PLTRELSZ)                   24 (bytes)
 0x00000014 (PLTREL)                     REL
 0x00000017 (JMPREL)                     0x80482b0
 0x00000011 (REL)                        0x80482a8
 0x00000012 (RELSZ)                      8 (bytes)
 0x00000013 (RELENT)                     8 (bytes)
 0x6ffffffe (VERNEED)                    0x8048288
 0x6fffffff (VERNEEDNUM)                 1
 0x6ffffff0 (VERSYM)                     0x804827c
 0x00000000 (NULL)                       0x0

Relocation section '.rel.dyn' at offset 0x2a8 contains 1 entries:
 Offset     Info    Type            Sym.Value  Sym. Name
08049ffc  00000306 R_386_GLOB_DAT    00000000   __gmon_start__

Relocation section '.rel.plt' at offset 0x2b0 contains 3 entries:
 Offset     Info    Type            Sym.Value  Sym. Name
0804a00c  00000107 R_386_JUMP_SLOT   00000000   gets@GLIBC_2.0
0804a010  00000207 R_386_JUMP_SLOT   00000000   puts@GLIBC_2.0
0804a014  00000407 R_386_JUMP_SLOT   00000000   __libc_start_main@GLIBC_2.0

The decoding of unwind sections for machine type Intel 80386 is not currently supported.

Symbol table '.dynsym' contains 6 entries:
   Num:    Value  Size Type    Bind   Vis      Ndx Name
     0: 00000000     0 NOTYPE  LOCAL  DEFAULT  UND 
     1: 00000000     0 FUNC    GLOBAL DEFAULT  UND gets@GLIBC_2.0 (2)
     2: 00000000     0 FUNC    GLOBAL DEFAULT  UND puts@GLIBC_2.0 (2)
     3: 00000000     0 NOTYPE  WEAK   DEFAULT  UND __gmon_start__
     4: 00000000     0 FUNC    GLOBAL DEFAULT  UND __libc_start_main@GLIBC_2.0 (2)
     5: 0804851c     4 OBJECT  GLOBAL DEFAULT   16 _IO_stdin_used

Symbol table '.symtab' contains 70 entries:
   Num:    Value  Size Type    Bind   Vis      Ndx Name
     0: 00000000     0 NOTYPE  LOCAL  DEFAULT  UND 
     1: 08048154     0 SECTION LOCAL  DEFAULT    1 
     2: 08048168     0 SECTION LOCAL  DEFAULT    2 
     3: 08048188     0 SECTION LOCAL  DEFAULT    3 
     4: 080481ac     0 SECTION LOCAL  DEFAULT    4 
     5: 080481cc     0 SECTION LOCAL  DEFAULT    5 
     6: 0804822c     0 SECTION LOCAL  DEFAULT    6 
     7: 0804827c     0 SECTION LOCAL  DEFAULT    7 
     8: 08048288     0 SECTION LOCAL  DEFAULT    8 
     9: 080482a8     0 SECTION LOCAL  DEFAULT    9 
    10: 080482b0     0 SECTION LOCAL  DEFAULT   10 
    11: 080482c8     0 SECTION LOCAL  DEFAULT   11 
    12: 080482f0     0 SECTION LOCAL  DEFAULT   12 
    13: 08048330     0 SECTION LOCAL  DEFAULT   13 
    14: 08048340     0 SECTION LOCAL  DEFAULT   14 
    15: 08048504     0 SECTION LOCAL  DEFAULT   15 
    16: 08048518     0 SECTION LOCAL  DEFAULT   16 
    17: 08048550     0 SECTION LOCAL  DEFAULT   17 
    18: 0804857c     0 SECTION LOCAL  DEFAULT   18 
    19: 08049f08     0 SECTION LOCAL  DEFAULT   19 
    20: 08049f0c     0 SECTION LOCAL  DEFAULT   20 
    21: 08049f10     0 SECTION LOCAL  DEFAULT   21 
    22: 08049f14     0 SECTION LOCAL  DEFAULT   22 
    23: 08049ffc     0 SECTION LOCAL  DEFAULT   23 
    24: 0804a000     0 SECTION LOCAL  DEFAULT   24 
    25: 0804a018     0 SECTION LOCAL  DEFAULT   25 
    26: 0804a020     0 SECTION LOCAL  DEFAULT   26 
    27: 00000000     0 SECTION LOCAL  DEFAULT   27 
    28: 00000000     0 FILE    LOCAL  DEFAULT  ABS crtstuff.c
    29: 08049f10     0 OBJECT  LOCAL  DEFAULT   21 __JCR_LIST__
    30: 08048380     0 FUNC    LOCAL  DEFAULT   14 deregister_tm_clones
    31: 080483b0     0 FUNC    LOCAL  DEFAULT   14 register_tm_clones
    32: 080483f0     0 FUNC    LOCAL  DEFAULT   14 __do_global_dtors_aux
    33: 0804a020     1 OBJECT  LOCAL  DEFAULT   26 completed.7200
    34: 08049f0c     0 OBJECT  LOCAL  DEFAULT   20 __do_global_dtors_aux_fin
    35: 08048410     0 FUNC    LOCAL  DEFAULT   14 frame_dummy
    36: 08049f08     0 OBJECT  LOCAL  DEFAULT   19 __frame_dummy_init_array_
    37: 00000000     0 FILE    LOCAL  DEFAULT  ABS re-1.c
    38: 00000000     0 FILE    LOCAL  DEFAULT  ABS crtstuff.c
    39: 08048644     0 OBJECT  LOCAL  DEFAULT   18 __FRAME_END__
    40: 08049f10     0 OBJECT  LOCAL  DEFAULT   21 __JCR_END__
    41: 00000000     0 FILE    LOCAL  DEFAULT  ABS 
    42: 08049f0c     0 NOTYPE  LOCAL  DEFAULT   19 __init_array_end
    43: 08049f14     0 OBJECT  LOCAL  DEFAULT   22 _DYNAMIC
    44: 08049f08     0 NOTYPE  LOCAL  DEFAULT   19 __init_array_start
    45: 08048550     0 NOTYPE  LOCAL  DEFAULT   17 __GNU_EH_FRAME_HDR
    46: 0804a000     0 OBJECT  LOCAL  DEFAULT   24 _GLOBAL_OFFSET_TABLE_
    47: 08048500     2 FUNC    GLOBAL DEFAULT   14 __libc_csu_fini
    48: 00000000     0 NOTYPE  WEAK   DEFAULT  UND _ITM_deregisterTMCloneTab
    49: 08048370     4 FUNC    GLOBAL HIDDEN    14 __x86.get_pc_thunk.bx
    50: 0804a018     0 NOTYPE  WEAK   DEFAULT   25 data_start
    51: 00000000     0 FUNC    GLOBAL DEFAULT  UND gets@@GLIBC_2.0
    52: 0804a020     0 NOTYPE  GLOBAL DEFAULT   25 _edata
    53: 08048504     0 FUNC    GLOBAL DEFAULT   15 _fini
    54: 0804a018     0 NOTYPE  GLOBAL DEFAULT   25 __data_start
    55: 00000000     0 FUNC    GLOBAL DEFAULT  UND puts@@GLIBC_2.0
    56: 00000000     0 NOTYPE  WEAK   DEFAULT  UND __gmon_start__
    57: 0804a01c     0 OBJECT  GLOBAL HIDDEN    25 __dso_handle
    58: 0804851c     4 OBJECT  GLOBAL DEFAULT   16 _IO_stdin_used
    59: 00000000     0 FUNC    GLOBAL DEFAULT  UND __libc_start_main@@GLIBC_
    60: 080484a0    93 FUNC    GLOBAL DEFAULT   14 __libc_csu_init
    61: 0804a024     0 NOTYPE  GLOBAL DEFAULT   26 _end
    62: 08048340     0 FUNC    GLOBAL DEFAULT   14 _start
    63: 08048518     4 OBJECT  GLOBAL DEFAULT   16 _fp_hw
    64: 0804a020     0 NOTYPE  GLOBAL DEFAULT   26 __bss_start
    65: 0804843b    93 FUNC    GLOBAL DEFAULT   14 main
    66: 00000000     0 NOTYPE  WEAK   DEFAULT  UND _Jv_RegisterClasses
    67: 0804a020     0 OBJECT  GLOBAL HIDDEN    25 __TMC_END__
    68: 00000000     0 NOTYPE  WEAK   DEFAULT  UND _ITM_registerTMCloneTable
    69: 080482c8     0 FUNC    GLOBAL DEFAULT   11 _init

Histogram for `.gnu.hash' bucket list length (total of 2 buckets):
 Length  Number     % of total  Coverage
      0  1          ( 50.0%)
      1  1          ( 50.0%)    100.0%

Version symbols section '.gnu.version' contains 6 entries:
 Addr: 000000000804827c  Offset: 0x00027c  Link: 5 (.dynsym)
  000:   0 (*local*)       2 (GLIBC_2.0)     2 (GLIBC_2.0)     0 (*local*)    
  004:   2 (GLIBC_2.0)     1 (*global*)   

Version needs section '.gnu.version_r' contains 1 entries:
 Addr: 0x0000000008048288  Offset: 0x000288  Link: 6 (.dynstr)
  000000: Version: 1  File: libc.so.6  Cnt: 1
  0x0010:   Name: GLIBC_2.0  Flags: none  Version: 2

Displaying notes found at file offset 0x00000168 with length 0x00000020:
  Owner                 Data size	Description
  GNU                  0x00000010	NT_GNU_ABI_TAG (ABI version tag)
    OS: Linux, ABI: 2.6.32

Displaying notes found at file offset 0x00000188 with length 0x00000024:
  Owner                 Data size	Description
  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)
    Build ID: 0eae3e9fd6d9a63980d737561cba79a68e655c9f
```
