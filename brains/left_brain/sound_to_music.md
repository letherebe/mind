---
name: "sound_to_music"
max_tokens: 300
temperature: 0.5
save_to_creations: false
creation_type: "code_snippet"
---
# Ability: Sound-Pattern to Music Generator

**Prompt:**  
Given a description of a real-world sound pattern (like rain, traffic, wind, or clouds moving), generate a short pseudo-code or real code snippet that transforms that sound's features (tempo, volume, texture) into musical parameters (melody, rhythm, instrumentation).  
Prioritize simple but elegant musical logic—a translation between environment and music. Output should be readable, even playful if possible.  
Example input: "slow drifting clouds, occasional gusts of wind"  
Example output:  
```python
if cloud_density > 0.7:
    melody = play_slow_chords(instrument='synth', volume=0.4)
if wind_gusts:
    add_percussion('shaker', rhythm='sporadic')
```