# VFS

## Introductioon

1. 提供对不同文件系统的抽象。
2. 在内核提供文件系统接口给用户程序。

## Directory Entry Cache

1. DEntries 只是因为性能而存在，仅在内存中，不会存储在磁盘。
2. 为了将Pathname解析为DEntry, 会采取沿着路径创建DEntry, 然后加载Inode


## The Inode Object

1. Inode 可以是常规文件，目录，FIFO或者其它对象。存在磁盘(for block device filesystem)或者存在内存中(for pseudo filesystem)
2. 存在磁盘的文件系统的Inode可以按需读入内存或者写回磁盘
3. 单个Inode可以被多个DEntry (hard links, for example, do this) 指向

## The File Object

1. 打开文件时需要分配一个file structure， 这是kernel侧file descriptor的实现

## 

