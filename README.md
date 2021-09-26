# euroTruckSimulator2_AutoPilot
Truck autopilot based on the in-game minimap.   
This is more a lane-assistant, I find it extremly useful on highways:   
1. You can use this program to help you stay in the lane even if you get distracted, 
1. Let the truck go on its own. My advice is to cruise control at about 70km/h(43.5mp/h).   
It still works at 100mk/h+, but it will crash into slower veichle since this program cannot make overtakes while truck is travelling on its own.    
Probably you should change values at line 46(miniMap = np.array(ImageGrab.grab(bbox=(2160,1100,2342,1160)))) because this parameters works for 2k monitors   
Another thing I've noticed is the fact that for each truck, different parameters work in different way.
