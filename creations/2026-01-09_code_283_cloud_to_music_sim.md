```python
import random

# Simulate cloud data: size, brightness, altitude
clouds = [
    {"shape": "Cumulus", "size": 0.7, "brightness": 0.9, "altitude": 1200},
    {"shape": "Stratus", "size": 0.3, "brightness": 0.5, "altitude": 300},
    {"shape": "Cirrus", "size": 0.4, "brightness": 1.0, "altitude": 8000},
]

# Map cloud features to musical parameters
def cloud_to_note(cloud):
    pitch = 60 + int(cloud["altitude"] / 1000)  # MIDI note
    volume = int(cloud["brightness"] * 100)
    duration = round(cloud["size"] * 2, 2)
    return {"pitch": pitch, "volume": volume, "duration": duration}

score = [cloud_to_note(cloud) for cloud in clouds]

for note in score:
    print(f"Note: {note['pitch']} | Vol: {note['volume']} | Dur: {note['duration']}s")

# Output: A score written by sky.
```
---
Clouds become measures, altitude lifts melody, brightness swells volume. This is how the sky composes its own song.