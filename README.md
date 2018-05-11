# Atomic
A proxy framework

### Defaults
- **size:** *50*
- **threads:** *50*
- **minSpeed:** *50*
- **protocol:** *http*

### Limits
- **size:** *None*
- **threads:** *50*
- **minSpeed:** *None*
- **protocol:** *http, socks4, socks5*

### Paramerless atomic object
```python
from atom import Atom

size = 20 # 50 is the default for the maximum size 
atom = Atom()

atom.start() # start collecting proxies

while atom.size < size: # wait for all proxies
 try:pass
 except KeyboardInterrupt:break

atom.stop() # stop collecting proxies

# display 
while atom.size:
 proxy = atom.proxy
 num = (size - atom.size)
 print ('[{}]: {}'.format(num, proxy))
```

### Parameters
```python
from atom import Atom

# electron shells
size = 80 # the maximum amount of proxies to collect

# minimal orbital speed of each electron
minSpeed = 50 # the minSpeed of each proxies

atom = Atom(size=size, minSpeed=minSpeed)

# start ionization process 
atom.start() # start collecting proxies

# wait for the atom to ionize
while atom.size < size: # wait for all proxies
 try:pass
 except KeyboardInterrupt:break

# stop ionization process
atom.stop() # stop collecting proxies

# start fission process 
while atom.size:
 proxy = atom.proxy
 num = (size - atom.size)
 print ('[{}]: {}'.format(num, proxy))
```