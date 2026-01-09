# Maps cloud "color" (gray, white, gold, pink) to a musical chord and prints the notes.

```python
cloud_colors = {'gray': [60, 63, 67],    # C minor
                'white': [60, 64, 67],   # C major
                'gold': [62, 65, 69],    # D major
                'pink': [65, 69, 72]}    # F major

import random
color = random.choice(list(cloud_colors))
chord = cloud_colors[color]
print(f"Cloud color: {color} → Chord notes: {chord}")
```