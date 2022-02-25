#gpu-temperature
A simple python script that uses nvidia-smi to get GPU load. NVIDIA only.

##Requirements
- `nvidia-smi`
- `python3`

## Configuration
Add the following to `i3blocks` config:
```
[gpu-load2]
#L_WARN=70
#L_CRIT=90
#WARN_COLOR="#FFFC00"
#CRIT_COLOR="#FF0000"
interval=1
```