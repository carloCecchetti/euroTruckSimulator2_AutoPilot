
# euroTruckSimulator2_AutoPilot
Truck autopilot based on the in-game minimap.   
This is more a lane-assistant than an autopilot, but I find it extremly useful on highways: 

* You can use this program to help you stay in the lane even if you get distracted.  
* Let the truck go on its own. My advice is to cruise control at about 70 km/h (45 mp/h).   

It still works at 100mk/h+, but it will crash into slower veichle since this program cannot make overtakes while truck is travelling on its own.    

# Solutions to common problems:

### Program gives me error as soon as I run it
- Probably you should change values at **line 46** (miniMap = np.array(ImageGrab.grab(bbox=(2160,1100,2342,1160)))) because this parameters works for 2k resolution. 

### Truck wobbles on straight
- Different parameters work in different way for each truck. You might want to change values at **line 46** (miniMap = np.array(ImageGrab.grab(bbox=(2160,***1100***,2342,1160)))). The lower the bold number, the less wobblier will be the truck on straight but might have some issues when the road makes sharp turns.

- **line41** time.sleep(difference/***5500***): The higher the number, the smaller will be correction. This makes the truck less wobbler on straight but probably it won't be able to turn enough in sharp turns.

### Truck isn't centered
- Based on how wide you set the miniMap capture window, basePoint value will change when in idle, so you might want to change values at ***lines 56 and 57, lines 59 and 60**.
1. While the program isn't running, place the truck in order to make the blue arrow on the mini map in the right middle of the red path (green tringles may help). 
2. Run the program and read basePoint value, it'll be you center value.
3. line 56 and 57 will be that previous value + 1 or 2.
4. line 59 and 60 will be that previous value - 1 or 2.
