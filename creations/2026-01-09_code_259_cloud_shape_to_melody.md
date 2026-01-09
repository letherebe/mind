```python
# Maps random cloud "shapes" (circles, lines, blobs) to different musical motifs and prints the melody notes.
import random

shapes = ['circle', 'line', 'blob']
motifs = {'circle': [60, 64, 67, 72], 'line': [60, 62, 64, 65, 67], 'blob': [60, 63, 65, 68]}
cloud = random.choice(shapes)
melody = motifs[cloud]
print(f"Cloud shape: {cloud} → Melody: {melody}")
```