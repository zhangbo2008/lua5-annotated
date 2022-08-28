https://github.com/hilarryxu/lua-5.3-annotated 原始地址.

 apt-get install libreadline-dev 
 make

我们跟着这个教程走.
https://blog.csdn.net/initphp/category_9293184.html

首先教程先直接粗略读一遍做一个整体把握.然后跟着教程顺序研究源码.
上来就是lua.h 研究里面头文件. 看个大概即可.不是c文件都看个大概.知道都有什么就完事.
然后lstate.c



## Lua源码阅读顺序

### 1. **lmathlib.c, lstrlib.c:**
>get familiar with the external C API. Don't bother with the pattern matcher though. Just the easy functions.

### 2. **lapi.c:**
>Check how the API is implemented internally. Only skim this to get a feeling for the code. Cross-reference to *lua.h* and *luaconf.h* as needed.

### 3. **lobject.h:**
>tagged values and object representation. skim through this first. you'll want to keep a window with this file open all the time.

### 4. **lstate.h:**
>state objects. ditto.

### 5. **lopcodes.h:**
>bytecode instruction format and opcode definitions. easy.

### 6. **lvm.c:**
>scroll down to luaV_execute, the main interpreter loop. see how all of the instructions are implemented. skip the details for now. reread later.

### 7. **ldo.c:**
>calls, stacks, exceptions, coroutines. tough read.

### 8. **lstring.c:**
>string interning. cute, huh?

### 9. **ltable.c:**
>hash tables and arrays. tricky code.

### 10. **ltm.c:**
>metamethod handling, reread all of *lvm.c* now.

### 11. **lapi.c**

### 12. **ldebug.c:**
>surprise waiting for you. abstract interpretation is used to find object names for tracebacks. does bytecode verification, too.

### 13. **lparser.c, lcode.c:**
>recursive descent parser, targetting a register-based VM. start from chunk() and work your way through. read the expression parser and the code generator parts last.

### 14. **lgc.c:**
>incremental garbage collector. take your time.

---
Read all the other files as you see references to them. Don't let your stack get too deep though.

"# lua5-annotated" 
