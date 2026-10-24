v1.1 - Aug 18th, 2026.  
  
- bug fix: voice stealing pops - modify voice stealing algo to add kill phase.  
- reduce dsp chunk size to 512.  
- set FX .dsp sample rate to match main .dsp.
  
### NOTE - this firmware is flawed
It requires to update config.txt on the SD Card, or you will get some glitching after 60 seconds.
on line 15 add `force_turbo=1` to fix it, but 1.2 fixes it in a better way.