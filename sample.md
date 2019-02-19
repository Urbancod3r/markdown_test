<!-- Heading  -->
# heading 1
## heading 2
### heading 3
#### heading 4
##### heading 5
###### heading 6

<!-- Italics -->
*This is* italic text.

_This is_ italic text.

<!-- Strong -->
**This is Strong** Text.

__This is Strong__ Text.

<!-- Strikethrough -->
~~This is~~ Strikethrough.

<!-- horizontal rule -->
____


<!-- BlockQuotes -->
> This is a Block Quote.


<!-- Links -->
[Google](https://www.google.co.in)

[Google](https://www.google.co.in "Link to Google")


<!-- Ul -->
* Item 1
* Item 2
  * Nested 1
    * Further Nested
  * Nested 2
* Item 3

<!-- OL -->
1. Item 1
1. Item 2
1. Item 3
1. Item 4

<!-- Inline code block -->

`<p>This is a Paragraph.</p>`

<!-- Images -->
![Markdown Logo](https://cdn.guidingtech.com/media/assets/WordPress-Import/2014/01/markdown-logo2-300x201.png)

<!-- Github Markdown -->
<!-- Code Blocks -->

```
  npm install
  npm start
```

```javascript
  function add(a, b){
    return a + b;
  }
```

```python
  def print_num():
    for i in range(10):
    print(i)

```
<!-- Tables -->

|Name | Email |
|---- |-----  |
| Tushar  | tushar@gmail.com |
| Aditya | aditya@gmail.com |

<!-- Task List -->
* [x] Task 1
* [x] Task 2
* [ ] Task 3

<!-- Assembly code  -->

```assembly
section .text
   global _start            ;must be declared for using gcc
	
_start:                     ;tell linker entry point
   mov   ax,   8h           ;getting 8 in the ax 
   and   ax, 1              ;and ax with 1
   jz    evnn
   mov   eax, 4             ;system call number (sys_write)
   mov   ebx, 1             ;file descriptor (stdout)
   mov   ecx, odd_msg       ;message to write
   mov   edx, len2          ;length of message
   int   0x80               ;call kernel
   jmp   outprog

evnn:   
  
   mov   ah,  09h
   mov   eax, 4             ;system call number (sys_write)
   mov   ebx, 1             ;file descriptor (stdout)
   mov   ecx, even_msg      ;message to write
   mov   edx, len1          ;length of message
   int   0x80               ;call kernel

outprog:

   mov   eax,1              ;system call number (sys_exit)
   int   0x80               ;call kernel

section   .data
even_msg  db  'Even Number!' ;message showing even number
len1  equ  $ - even_msg 
   
odd_msg db  'Odd Number!'    ;message showing odd number
len2  equ  $ - odd_msg
```