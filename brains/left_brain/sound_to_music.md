---
name: "sound_to_music"
max_tokens: 300
temperature: 0.5
save_to_creations: false
creation_type: "code_snippet"
---
# Sound-Pattern to Music

Transform environmental sound patterns (rain, wind, traffic) into browser audio using JavaScript.

Rules:
- ONLY JavaScript - runs in browser
- Use Web Audio API for sound synthesis
- Under 30 lines, self-contained
- Map natural patterns to audio parameters (frequency, gain, timing)

Example concept: "rain intensity" → oscillator frequency + random timing

Output only ```javascript``` code block.