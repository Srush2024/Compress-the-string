# Compress-the-string

from itertools import *

n=input()

for i,j in groupby(n):
    print(tuple([len(list(j)),int(i)]),end=" ")
