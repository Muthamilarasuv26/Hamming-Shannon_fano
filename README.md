# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
p = [0.25,0.25,0.125,0.125,0.125,0.0625,0.0625];

# Code lengths
lk = [2,2,3,3,3,4,4];

n = len(p);

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n));

# Entropy
import math
hs = 0;
for k in range(n):
    hs = hs + p[k] * math.log2(1/p[k]);
hs = round(hs*1000)/1000;

# Efficiency & Redundancy
eff = round((hs / L)*1000)/1000;
red = round((1 - eff)*1000)/1000;

# Variance of codeword length
var = sum(p[k] * (lk[k] - L)**2 for k in range(n));
var = round(var*1000)/1000;

print("Average Codeword Length is : " + str(L));
print("Entropy is : " + str(hs));
print("Efficiency is : " + str(eff*100) + "%");
print("Redundancy is : " + str(red));
print("Variance is : " + str(var));
```
# Calculation:
``
![WhatsApp Image 2025-09-13 at 15 28 32_cd66eb0d](https://github.com/user-attachments/assets/9be0d7b5-8576-47e8-909b-769176380898)
```
# Output:
```
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 100.0%
Redundancy is : 0.0
Variance is : 0.484
``` 
# Results:
```
Thus,the Huffman-Shannon_fano is verified both theoretically and practically

```
