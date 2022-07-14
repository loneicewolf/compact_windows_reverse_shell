order does matter!
```
#                            vvvvvvv
me :~$ i686-w64-mingw32-gcc -lws2_32  -o A a.c
        /usr/bin/i686-w64-mingw32-ld: /tmp/ccAQV9Ws.o:a.c:(.text+0x9a): undefined reference to `_imp__WSAStartup@8'
        /usr/bin/i686-w64-mingw32-ld: /tmp/ccAQV9Ws.o:a.c:(.text+0xd3): undefined reference to `_imp__WSASocketW@24'
        /usr/bin/i686-w64-mingw32-ld: /tmp/ccAQV9Ws.o:a.c:(.text+0x109): undefined reference to `_imp__inet_pton@12'
        /usr/bin/i686-w64-mingw32-ld: /tmp/ccAQV9Ws.o:a.c:(.text+0x129): undefined reference to `_imp__htons@4'
        /usr/bin/i686-w64-mingw32-ld: /tmp/ccAQV9Ws.o:a.c:(.text+0x172): undefined reference to `_imp__WSAConnect@28'
        collect2: error: ld returned 1 exit status

#                                      vvvvvvv
me :~$ i686-w64-mingw32-gcc  -o A a.c -lws2_32

```
