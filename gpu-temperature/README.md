#gpu-temperature
A simple python script that uses nvidia-smi to get GPU thermals.

##Requirements
- `nvidia-smi`
- `python3`

## Configuration
Add the following to `i3blocks` config:
```
[gpu-temperature]
#T_WARN=70
#T_CRIT=90
#WARN_COLOR="#FFFC00"
#CRIT_COLOR="#FF0000"
interval=1
```