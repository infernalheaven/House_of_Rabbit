# House of Rabbit

Heap exploitation technique bypassing ASLR

## Description

This is a heap exploitaion technique that connects chunks with very large sizes to largebins.
By maximizing the size of the fake chunk prepared for the known address, it is possible to return an arbitrary address in malloc by going round the address space.

## Features

- Arbitary address can be returned with malloc
- It is unnecessary to specify the address where the Heap area is located

## Constraints

- You can call any size malloc, and free
- You can freely write 0x20 bytes or more for known addresses
- There is a vulnerability that can rewrite fd of fastbins

## Author

[@shift\_crops](https://twitter.com/shift_crops)
