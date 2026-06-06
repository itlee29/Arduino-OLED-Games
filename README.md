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

The second game is a spinoff of the chrome dino game, with many of the effects such as ducking, jumping, and even night/day cycles! I made this in 8th grade for the first version of my platformer. Press on the joystick's button to duck, and press on the main button to jump! If you collect powerups, you can use them by shifting the joystick right (I think). Depending on your version of the console, you might have to use the version with (1) instead of the base version of the chrome dino game, as the one with (1) has certain settings switched, including the button joystick.

The third game is a spinoff of Moon Lander, where you press the button to fly up, and navigate left and right with the joystick. Try to softly land on the pad, but watch out, as you can run out of fuel! The fuel bar is on the right.

The final game is my best, my platformer. This features a full in-depth level editor online; by editing the 7 massive arrays at the beginning of the code, you can change their values from 0-9,A-E (sorta like hexadecimal), to represent different platforms. There is an empty platform that you can replace any of the pre-built platforms with at the beginning. The platform definitions are as follows:
0 is blank, 
1 is a wall, 
2 is a spike, 
3 is a horizontal enemy, 
4 is a vertical enemy, 
5 is the end of the level, 
6 horizontal moving platform, 
7 is vertical moving platform, 
8 is jump through platform, 
9 is a bounce collider - bounces up
A is Jumper - sends you flying up
B is water - infinite jump + reduced gravity
C is blasterright
D is blasterleft
E is powerup
As you can see, this is a very expansive game! This is an example level you could use. Basically, paste this into a text editor, and then replace the 0's with your level! Then, replace Blanklevel with the level number (like level1, level2...), paste it in, deleting the existing level and then play!:
static const byte Blanklevel[LEVELMAXUP][LEVELMAXRIGHT] PROGMEM = {
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,},
{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,}
};
As you can see, this is a very in-depth game T_T
