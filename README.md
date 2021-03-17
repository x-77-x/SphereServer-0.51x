# SphereServer-0.51x
Potential Update to the Recovered 0.51a (0.52) Source

SPHERESERVER 0.51x  WISHLIST  (3/17/21)
-----------------------------
-HITPOINTS - on NPCS, there needs to be a seperation between STR and hitpoints, 
       i want npc characters with 200STR AND 1000hp.
	    by default the hitpoints will drain until they are equal with STR. so add...
MAXHITS=1000
MAXSTAM=1000
MAXMANA=1000
???

so if players and npcs are over their maxhits, hp drains to equal their maxhits
and if players and npcs are under their maxhits, they heal to equal their maxhits

FOR PLAYERS i want players to have x2 for hitpoints, stamina, mana
so 
125 STR = 250 hitpoints
125 DEX = 250 stamina
125 INT = 250 mana


-sphere to run in the notification area next to the clock!!!


-sphere script loading times are abnormally slow compared to the 51a release version


-Provocation - you can use provoc on player in guarded area, then call guards on them after it makes you attack them
		check area for guards?  maybe cant be used on other players?  not really sure how provoc is supposed to work,
		but i know i disabled it 18 years ago for a reason

-Poison - when posion is cast on someone, the timer on the memory item is 120 ticks before the poison effect starts.
		thats way too long, also poison needs to be dehardcoded so the different posion levels damages can be adjusted
[ FIXED!!! ]    

-yell distance! ! it would be nice to adjust the distance when players yell in game 20 squares, 50 squares, ect...
		players can communicate cross map by yelling =P
[ FIXED!!! ]


-colored SYSMESSAGE, that lil sphere im using has it... looks like this
SRC.SYSMESSAGE #0033,3, You have gained a reward!


-TAG.NAME.HUE 021   nice to be able to change the color of NPCs name


-Tracking - make sure "tracking players" actually track players only, ect... (i remember something wrong with tracking)


-Show damage above npc when attacked  (like LiL Sphere)


-no shooting arrows through multis floors!
example... put a npc on the roof of a tower, you can shoot him from the 1st floor


-see whos online?  maybe a way to see whos online?  .online command
maybe just use the hardcoded .admin menu and remove account information, maybe just a simple list with only characters names


the greatest thing about the new sphere is [FUNCTION  f_xxx]
you can make your own functions and solve just about any problem with a function
and TAG.YOURMOM=1 same as VAR. i think, but permanent, great way to tag characters and items for scripting


-when you run from an npc with a bow, he shoots a shitton of arrow animations,  you get hit multiple times


-SECURITY!!! im sure all those antique injection hacks still work


-tighten up loose ends, make sure all the skills do what they are supposed to =)


-tillerman, arent you supposed to pin a map and drop it on the tiller man and hes supposed to go there?


-colored multis??? new sphere you can go debug mode and set the color on a multi and it will change color in game
after 17 years i just realized you can dye a ship deed and the multi will be affected, but only the parts are colored =)


-weapon speed? i dont think speed= works, you adjust the speed by the weapon weight, which kinda makes sense =P


-books?  the books in SPHEREBook.scp never worked, the pages are empty in game


-explosion potions, be able to set the low and high damage. you can raise the more 2, but the range is so big


-walk and shoot would be nice, half accuracy when moving?


NEW TRIGGERS
--items--
ONTRIGGER=CLICK  (single click)  colored  NAME.HUE!?

ONTRIGGER=DROPON_SELF
	heres a nice lil bag script in the new sphere that will let you only drop runes in a bag
	ON=@DROPON_SELF
	IF !(<ARGO.TYPE>==t_rune)
	SRC.SYSMESSAGE You may only place runes inside this bag.
	RETURN 1
	ENDIF

since there is no runebooks in 51a, a newbied bag that will only accept runes would be nice


--characters--
ON=@LOGIN

ON=@LOGOUT

ON=@GetHit

a trigger so NPCS will look at eachother ON=@SeeNewNPC ?  a way to get npcs to fight (besides berserker brain)

ON=@NotoSend
another nice one that will change the color of a moused over character
	ON=@NotoSend//2 ALLY 5 ENEMY 6 RED	
	IF (<SRC.TAG0.MILITARY>)
		IF !(<SRC.TAG0.ARMYNUMBER>==<TAG0.ARMYNUMBER>)
		//IF !<GUILD>
		ARGN1=5
		ELIF (<SRC.TAG0.ARMYNUMBER>==<TAG0.ARMYNUMBER>)
		//ELIF <GUILD>
		ARGN1=2
		ENDIF
	ENDIF
  
  
  SUMMARY - basically Lil Sphere by Fallout added some nice features to 0.51a, id like to add those features
  and add a few new things and tidy up the 0.51a source for those who still have old server files...
  for those who dont know... there was a re-write 0.53 that changed the structure for what we know as the modern versions of Sphere, that
  0.53 is what lead up to 55i version alot of people used, this was BEFORE that... servers that used TUS, GreyServer, 0.48e. 0.51a... 1998 to 2000
  
https://web.archive.org/web/19991013081655/http://menasoft.com:80/

https://web.archive.org/web/20001009023001/http://menace.ne.mediaone.net/spheres1.htm

https://web.archive.org/web/20000706193639/http://menace.ne.mediaone.net/

https://web.archive.org/web/20000819050744/http://www.sphereserver.com/
