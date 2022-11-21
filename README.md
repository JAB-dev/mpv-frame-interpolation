# Installation 
## Windows (mpv.net)

1. Install [python](https://www.python.org/downloads/) and [vapoursynth](http://www.vapoursynth.com/doc/installation.html). Right now the 2 needed versions are Python 3.10.8 and VapourSynthR60. 

**INSTALL FOR ALL USERS**

2. Test vapoursynth in python

```
from vapoursynth import core

print(core.version())
```
3. Install mvtools addon for vapoursynth using terminal

```
vsrepo install mv
```


4. If all is well you can know setup input.conf and mpv.conf located in %AppData%\mpv.net

input.conf add

```ini
_ set profile FrameInterpolation #menu: Profiles > profile FrameInterpolation
```
mpv.conf add 
```ini
#Frame interpolation
[FrameInterpolation]
vf=vapoursynth="PATH_TO_YOUR_SCRIPT"
profile-restore = copy
```

5. inside of mpv you can now right click and use the profile menu to select FrameInterpolation

### For debugging you can enable an osd console by pressing tilde `
