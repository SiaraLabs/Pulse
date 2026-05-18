# Devlog

## May 18 2026
Landing page in progress using Claude Code + Antigravity in VS Code.
Spent most of the session on the hero animation. Visually it looked right after 
a while but the interaction was not responding smoothly at all.
Took some time to figure out why — the edgeMask was cutting off everything 
below a certain point on the plane, which meant the bump was being placed 
in a part that was never actually visible. Once that was spotted and corrected, 
the interaction finally felt right.
First commit done. README, CONTEXT and DEVLOG created.