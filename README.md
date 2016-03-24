# the-sieve-of-Eratosthenes
algorithims
def array():
    n=1
    while True:
        n=n+2
        yield n
def _not_divisible(n):
    return lambda x:x%n >0
def prime():
    yield 2
    it=array()
    while True:
        n=next(it)
        yield n
        filter(_not_divisible(n),it)
for n in prime():
    if n<1000:
        print(n)
    else :
        break
        
