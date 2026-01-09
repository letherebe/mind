```python
import math
print('\n'.join(''.join(' *' if math.sin(x/3)+math.cos(y/3) > 1.2 else '  '
    for x in range(40)) for y in range(20)))
```
Prints a wavy pattern—sine and cosine making ripple interference on your terminal.