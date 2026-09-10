## Decimal to binary
- 10 = 00001010
- 210 = 11010010
- 168 = 10101000
- 16 = 0000100
- 255 = 11111111
- 128 = 10000000
- 192 = 11000000
- 248 = 11111000
- 0 = 00000001

---
- To get these results, I took a number and divided it by 2 each time till it turns into 0. Depending on the number I got, I wrote down 0 (if the number was even) or 1 (if the number was odd). Then I’ll simply mirror the final result I’ve got.
- For example, 10. 10 is even so I wrote 0, then 10/2=5, 5 is odd so I wrote 1 and so on till 0, and 0 is odd so I write 1. I have got this result: 0101. Next, I simply add zeros until the number has eight digits (01010000). Then I simply reverse the number, and here is the result: 00001010.

## Binary to decimal
- 11000000 = 192
- 11111111 = 255
- 10101000 = 168
- 00010000 = 16
- 11111000 = 248
- 11010010 = 210

---
- 
