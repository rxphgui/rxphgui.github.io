---
title: "Reverse_chall"
date: 2022-04-26T20:23:11+02:00
draft: true
---

Challenge de Reverse 

```Assembly
lea     rax, [rbp+s]
mov     rsi, rax
lea     rax, aHiThereS  ; "Hi there, %s !\n\n"
mov     rdi, rax        ; format
mov     eax, 0
call    _printf
mov     dword ptr [rbp+needle], 767A716Eh
mov     [rbp+var_32], 61h ; 'a'
lea     rax, [rbp+needle]
mov     rsi, rax
mov     edi, 0Dh
call    ces
lea     rdx, [rbp+needle]
lea     rax, [rbp+s]
mov     rsi, rdx        ; needle
mov     rdi, rax        ; haystack
call    _strstr
test    rax, rax
jz      loc_155D
``` 

