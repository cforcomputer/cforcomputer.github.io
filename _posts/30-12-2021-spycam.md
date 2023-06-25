---
layout: post
title: catching a thief
slug: the-spycam
---

date: Dec 30, 2021

skills used:
 - networking (server config)
 - PCB wiring
 - arduino coding
 - out-of-the-box thinking



### The oatmeal had vanished.

Nothing was off limits, the bag was less than a euro and the invisible thief had struck again. For months things had been going missing. From expensive meats, to yoghurt, to half eaten sandwiches. You couldn’t buy food, put it in the fridge or your box and expect it to still be there in the morning.

Was it one person? Multiple? Nobody could be sure, and mistrust had fouled the usually jubilant atmosphere of the StayOkay Hostel. We had been tolerating the theft for months, but as time progressed the thief grew increasingly emboldened in their success. Food was vanishing during the day a few hours after it had been bought.

The oatmeal was their final mistake. That seemingly inconsequential bit of food was what gave me the motivation to bust the traitor.

### Working the problem

I had to rapidly find a way to catch the thief, and the simplest way I could think of was with a hidden camera. Enter the all-in-one wonder-child the ESP32 microcontroller. After reaching out to my friends that specialize in electrical engineering, I was able to discover that this particular, $10 microcontroller had a built-in webcam, bluetooth, AND Wi-Fi hosting.

I ordered the controller, along with a power adapter for USB type-A to TTL Serial UART adapter, jumper cables, and a 20,000 mAh powerbank. The total cost was under $30.

After it arrived, I connected the microcontroller to the serial adapter and then flashed open source facial recognition AI project files to the microcontroller using the Arduino IDE. I used this particular code because it included a webserver that would stream the live video over the hostel Wi-Fi.

It was then a simple matter of obtaining the credentials of the hostel network. I could then view the camera feed from my laptop and record it from there. I didn’t have to deal with checking local storage. That way, if the camera was discovered and stolen as well, I would see their face.

I placed the setup in an empty egg carton with a small hole in the front for the camera. Then I placed it in my food box and left it overnight.

I dialled in the IP, the camera feed was grainy, but it was enough. The operation was a go. I hit the record button and went to sleep.

The next day, I giddily opened the save file on my computer.

### Results

The video had been corrupted. I was devastated. Then I remembered that I had woken up early in the morning, around 3:30 am to get a drink of water. I had paused and restarted the stream recording then.

I opened the broadcast software I was using to record called OBS, and saw with relief that the recording was still going. I crossed sweaty fingers and hit the stop button. The video file was nearly six hours long, but it successfully compiled.

The very first day, the very first test, and just ten minutes into the recording, I had him.

To be absolutely sure I had the right person, I dropped the bombshell that evening when everyone was eating dinner. “I may or may have footage of the thief taking everyone’s food.” I said slyly over a plate of chicken stirfry.

The reaction was instantaneous as the other students did a double take. Then they started to ask me in excitement if they could see the video. By the time I returned, everyone in the hostel was gathered around a table.

“I’m not absolutely sure it’s him,” I said cautiously, “but I want you guy’s to see if he’s taking your food or not.”

“That’s my chicken!” A girl cried out.

“Is that our box? That’s our box!”

“I’m gonna go show this man some Irish love.” A student said in a thick accent.

I had caught the thief. Or at least one of them.

Over the next few days, the manager of the hostel confronted the man and got him to admit that he had stolen our food, and that he wouldn’t steal anymore. A victory seeing that without the bluff, the footage could never be used legally. In a week he was gone.

I was praised and patted on the back. The mood had shifted, and I was met with glowing smiles and happy conversation. I did not gloat, or impress the need for favours. I sat and ate my oatmeal in peace.

Nobody’s food was ever stolen again.

### photos
![The original spy camera prototype](assets/images/projects/hacked-min.jpg)
![The ESP-32 chip](assets/images/projects/esp32.webp)
![The thief captured on camera](assets/images/projects/food-thief.webp)