---
title: tokenizer
draft: false
tags:
---
 
strings are sequences of unicode code points (unicode is a standard which defines what integers represent what character) Unicode text is processed and stored as binary data using encoding which translate the code points into sequences of bytes which the computer can understand and store in memory
the one used here is UTF - 8 (UTF-8 encodes code points in one to four bytes) because its variable length encoding unlike UTF - 32 and its backwards compatible (older encoding like ASCII works correctly using UTF - 8)

[Github](https://github.com/Blitzo125/Tokenizer)

I used UTF - 8 encoding and used [Byte Pair encoding](https://en.wikipedia.org/wiki/Byte-pair_encoding) which takes the two most frequent pairs of tokens and replaces them with a new token thus compressing the data so the we can have more data using less number of tokens
I used a dataset tiny Shakespeare and took first 50000 characters and merged on that 500 times
i converted the text to list of token id using UTF - 8 encoding

I made pairs of consecutive tokens and then counted there frequencies then replaced the top 10 most frequent tokes with new tokens starting from 256 (0-255 are ASCII bytes) for 500 iteration
after training this i got the following

Number of characters in tiny Shakespeare: 1115394 characters                                      
Total UTF-8 tokens in tiny Shakespeare : 1115394                                                             
Total number of tokens after Byte Pair encoding: 386452                                                
Overall compression: 65.4%                                                                                                  
Vocabulary range: 0 to 3348                                                                                                 

After that using Cursor assistant i made it a webpage and hosted it using github pages                                                                                                                                        
You can try it [Here](https://blitzo125.github.io/Tokenizer-web/)
