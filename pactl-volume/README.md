#pactl-volume
After a lot of trial and error with [pipewire-volume](https://github.com/vivien/i3blocks-contrib/tree/master/volume-pipewire) it failed to grab any volume info if no sound was playing. So I wrote a simple python script that uses `pactl` to figure out volume info for the default sink.

##Requirements
- `pactl`
- `python3`

## Configuration
Recommended to add the following to `i3` config:
```
# Pipewire-pulse
bindsym XF86AudioMute exec --no-startup-id pactl set-sink-mute 0 toggle && pkill -RTMIN+1 i3blocks
bindsym XF86AudioLowerVolume exec --no-startup-id pactl set-sink-volume 0 -5% && pkill -RTMIN+1 i3blocks
bindsym XF86AudioRaiseVolume exec --no-startup-id pactl set-sink-volume 0 +5% && pkill -RTMIN+1 i3blocks
```
Add the following to `i3blocks` config:
```
[pactl-volume]
interval=once
markup=pango
signal=1
## If SUBSCRIBE=1, set interval=persist
#SUBSCRIBE=0
## Warning color for volume >100%
#WARN_COLOR="#FFFC00"
## Warning color for volume >150%
#CRIT_COLOR="#FF0000"
```