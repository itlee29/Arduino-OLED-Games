Hi Everyone who's reading this!
I'm Isaac Lee - This is my repository for a few arduino games I've been working on. ALL of these should work as is,
however they probably require you to download the libraries.
Most of these work on an arduino NANO, however I will soon adapt them to work on a nano ESP32 too.

The wiring is as follows:
OLED 128 x 64 screen (any color): SDA -> A4, SCL -> A5
JOYSTICK: Y->A2, X->A1, Button:D3
BUTTON: S->D2

I may make a PCB incorperating these wirings if I feel like it!

Note - due to discrepancies between joysticks, the Y and X value of the joysticks MAY BE SWITCHED. In this case, kindly edit the code on your end and switch the values if you know how, or just rotate your joystick!

Quick discription of the games:

BATTLECATS_OLED was made on 6/6/2026 (wow nice date!). It is a fully functioning spinoff of the classic game "The Battle Cats."
While playing, you might see a few of your favorite characters too! It is currently in development, and this is the first 
version. You can move your joystick left and right to select cats, and press the button to deploy them. But watch out, because the enemy can deploy some pretty damaging cats too!. Reach and destroy your opponent's base to win, while guarding your own! There is currently no homescreen, however this may change. One last thing - due to memory constraints, it is impossible for either side to deploy more than 3 cats at once. In addition, as of right now, you can only select between wall cat and cat, and if you attempt to scroll further there will be nothing else.

The second game is a spinoff of the chrome dino game, with many of the effects such as ducking, jumping, and even night/day cycles! I made this in 8th grade for the first version of my platformer. Press on the joystick's button to duck, and press on the main button to jump! If you collect powerups, you can use them by shifting the joystick right (I think)
