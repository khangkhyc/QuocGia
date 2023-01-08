from random import randint
li = 10**7
m = 10**9+7
a = [randint(1,10**7) for i in range(10**3)]
ind = randint(1,10**3)
import time
start_time = time.time()

import math
ind -= 1
f = [[i,0] for i in range(3163)]
def primeFactors(n):
    c = 0
    while n % 2 == 0:
        c += 1
        n //= 2
    f[2][1] = max(c,f[2][1]) 
    for i in range(3, int(math.sqrt(n))+1, 2):
        c = 0
        while n % i == 0:
            c += 1
            n //= i
        f[i][1] = max(c,f[i][1]) 
    if n > 2 and n < 3163: f[n][1] = max(1,f[n][1])
for i in a: primeFactors(i)
n = a[ind]
while n % 2 == 0:
   f[2][1] -= 1
   n //= 2
for i in range(3,int(math.sqrt(n))+1,2):
   while n % i == 0:
      f[i][1] -= 1
      n //= i
if n > 2 and n < 3163: f[n][1] -= 1
pr = 1
for i in f:
   if i[1] % 2 == 0: pr *= i[0]**i[1]
print(pr%m)

end_time = time.time()
elapsed_time = end_time - start_time
print(f"Elapsed time: {elapsed_time:.2f} seconds")
