# handshake-hackerrank
To find out total handshakes


#!/bin/python3

import os
import sys

def handshake(n):
    if n==1:
        return 0
    elif n==2:
        return 1
    else:
        a=1
        b=1
        for i in range(1,n+1):
            a=a*i
        c=a
        for j in range(1,n-1):
            b=b*j
        d=b*2
        return (c//d)

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    t = int(input())

    for t_itr in range(t):
        n = int(input())

        result = handshake(n)

        fptr.write(str(result) + '\n')

    fptr.close()
