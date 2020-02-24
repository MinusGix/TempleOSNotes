(From [here](https://www.reddit.com/r/TempleOS_Official/comments/c98tvu/i_figured_out_how_to_get_60fps_in_templeos/))
You can change the FPS cap via two defines in `KernelA.HH`, on line 1478 there are two defines. 
```C
#define WINMGR_FPS  (30000.0/1001)
#define WINMGR_PERIOD (1001/30000.0)
```
Change the `3`'s to a `6` to change the cap to 60fps. Yes you can change it to higher (or lower) but you're unlikely to receive too much benefit past that.

You will need to reboot to experience the change. To confirm it's working, at the top there's a counter for FPS. Upon rebooting, it should stay basically on 60.
