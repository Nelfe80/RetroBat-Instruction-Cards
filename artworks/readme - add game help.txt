Adding a game is easy if you've identified the system.
You can already launch this line in powershell in the /emulators/mame folder:
 ./mame -lx <rom name without extension>.
This will identify the system and its available inputs, such as "SERVICE", "IN0", "IN1" and "IN2" or for NEOGEO ":edge:joy:JOY1", ":edge:joy:JOY2", ":edge:joy:START"
Next, here's a list of inputs for the most commonly used systems, but you should be aware that you may need to consult the Mame core sources to adjust certain parameters specific to certain games.
If you have an alternative rom version to the one shown here, simply rename the zip file or folder in artwork to make them work.

SYSTEM16 : Altered Beast, Golden Axe
https://github.com/mamedev/mame/blob/master/src/mame/sega/system16.cpp

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "SERVICE"
local player1_start_BITPORT = 0x10
local player1_keyup_IOPORT   = "P1"
local player1_keyup_BITPORT  = 0x20
local player1_keydown_IOPORT = "P1"
local player1_keydown_BITPORT= 0x10
-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "SERVICE"
local player2_start_BITPORT = 0x20
local player2_keyup_IOPORT   = "P2"
local player2_keyup_BITPORT  = 0x20
local player2_keydown_IOPORT = "P2"
local player2_keydown_BITPORT= 0x10


CPS1 : 
Carrier Air Wing, Cadillacs and Dinosaurs, Final Fight, Ghouls 'n Ghosts, Mercs, Street Fighter
https://github.com/mamedev/mame/blob/master/src/mame/capcom/cps1.cpp

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "IN0"
local player1_start_BITPORT = 0x10
local player1_keyup_IOPORT = "IN1"
local player1_keyup_BITPORT = 0x0008
local player1_keydown_IOPORT = "IN1"
local player1_keydown_BITPORT= 0x0004

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "IN0"
local player2_start_BITPORT = 0x20
local player2_keyup_IOPORT = "IN1"
local player2_keyup_BITPORT = 0x0800
local player2_keydown_IOPORT = "IN1"
local player2_keydown_BITPORT= 0x0400

OLD CPS1 :
Street Fighter
-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "SYSTEM"
local player1_start_BITPORT = 0x0001
local player1_keyup_IOPORT = "IN1"
local player1_keyup_BITPORT = 0x0008
local player1_keydown_IOPORT = "IN1"
local player1_keydown_BITPORT= 0x0004

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "SYSTEM"
local player2_start_BITPORT = 0x0002
local player2_keyup_IOPORT = "IN1"
local player2_keyup_BITPORT = 0x0800
local player2_keydown_IOPORT = "IN1"
local player2_keydown_BITPORT= 0x0400


CPS2 : Alien vs. Predator, Hyper Street Fighter II, Marvel Super Heroes, Marvel Vs Capcom, SFA
https://github.com/mamedev/mame/blob/master/src/mame/capcom/cps2.cpp

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "IN2"
local player1_start_BITPORT = 0x0100
local player1_keyup_IOPORT = "IN0"
local player1_keyup_BITPORT = 0x0008
local player1_keydown_IOPORT = "IN0"
local player1_keydown_BITPORT= 0x0004

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "IN2"
local player2_start_BITPORT = 0x0200
local player2_keyup_IOPORT = "IN0"
local player2_keyup_BITPORT = 0x0800
local player2_keydown_IOPORT = "IN0"
local player2_keydown_BITPORT= 0x0400

CPS3 : SFIII 
https://github.com/mamedev/mame/blob/master/src/mame/capcom/cps3.cpp

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "INPUTS"
local player1_start_BITPORT = 0x10000000
local player1_keyup_IOPORT = "INPUTS"
local player1_keyup_BITPORT = 0x00000001
local player1_keydown_IOPORT = "INPUTS"
local player1_keydown_BITPORT= 0x00000002

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "INPUTS"
local player2_start_BITPORT = 0x20000000
local player2_keyup_IOPORT = "INPUTS"
local player2_keyup_BITPORT = 0x00000100
local player2_keydown_IOPORT = "INPUTS"
local player2_keydown_BITPORT= 0x00000200

DECO32 : Captain America and the Avengers, 
https://github.com/mamedev/mame/blob/master/src/mame/dataeast/deco32.cpp

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "IN0"
local player1_start_BITPORT = 0x0080
local player1_keyup_IOPORT = "IN0"
local player1_keyup_BITPORT = 0x0001
local player1_keydown_IOPORT = "IN0"
local player1_keydown_BITPORT= 0x0002

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "IN0"
local player2_start_BITPORT = 0x8000
local player2_keyup_IOPORT = "IN0"
local player2_keyup_BITPORT = 0x0100
local player2_keydown_IOPORT = "IN0"
local player2_keydown_BITPORT= 0x0200

NEOGEO : Metal Slug, Samourai Shodown, 

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = ":edge:joy:START"
local player1_start_BITPORT = 0x0001
local player1_keyup_IOPORT = ":edge:joy:JOY1"
local player1_keyup_BITPORT = 0x0002
local player1_keydown_IOPORT = ":edge:joy:JOY1"
local player1_keydown_BITPORT= 0x0001

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = ":edge:joy:START"
local player2_start_BITPORT = 0x0100
local player2_keyup_IOPORT = ":edge:joy:JOY2"
local player2_keyup_BITPORT = 0x0002
local player2_keydown_IOPORT = ":edge:joy:JOY2"
local player2_keydown_BITPORT= 0x0001


CAVE : Pretty Soldier Sailor Moon
mame/src/mame/atlus/cave.cpp

-- Variables pour les entrées du joueur 1 (gauche)
local player1_start_IOPORT = "IN0"
local player1_start_BITPORT = 0x0080
local player1_keyup_IOPORT = "IN0"
local player1_keyup_BITPORT = 0x0001
local player1_keydown_IOPORT = "IN0"
local player1_keydown_BITPORT= 0x0002

-- Variables pour les entrées du joueur 2 (droite)
local player2_start_IOPORT = "IN1"
local player2_start_BITPORT = 0x0080
local player2_keyup_IOPORT = "IN1"
local player2_keyup_BITPORT = 0x0001
local player2_keydown_IOPORT = "IN1"
local player2_keydown_BITPORT= 0x0002

