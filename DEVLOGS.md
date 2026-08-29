# DEVLOGS:

---

> **Total Time Logged:** `i'm too lazy to calculate the total time each devlog so i'll calculate it at the end...`  
> **Repository:** [F-24-keeb](https://github.com/fork0m/F24-keeb)  
> **License:** [CC BY 4.0](LICENSE)

---

## 26.07.2026 - EST time: `3 hrs`
> Research
As today is the first day of my keyboard DIY journey i decided to start off with research and idea grounding. The only idea i had is that "I want it to have TWO function rows!", that's when I started designing the fisr prototype on [KLE](https://www.keyboard-layout-editor.com/#/), as of now, i'm proud to announce that the F-24-prototype-MK1 is done!

<img width="1073" height="411" alt="F-24-prototype-MK1" src="https://github.com/user-attachments/assets/829ca949-d6a2-449e-b788-5c58b400511d" />

it's still far from perfect and i'd say that it barrely represents my idea but it's easier to think when you have a graphical representation of your thoughts. Another thing that i slightly touched is the look, feel and design of the keyboard. Even though the real design will only be developed after the MVP (AKA the layout and the bare minimum of the PCB and case) is ready, i still wanted to have some references on what and how.
One of my favourite keyboard designs (and the one I use RN) is the Varmilo Summit R2 TKL:
<img width="894" height="336" alt="image" src="https://github.com/user-attachments/assets/497dd6e0-9236-40c8-85c1-93731d616c45" />
Just look at those colors! the designs and icons are also cool, i love that some function keys are replaced with icons (i'll probably do that too) and the ESC key... OMG it gorgeously stands out.

Another keyboard design I enjoyed is the Lofree Block:
<img width="894" height="384" alt="image" src="https://github.com/user-attachments/assets/1e0537f8-63e7-41d9-992a-064120320000" />
Assuming that most (if not all) double F row keyboards are old as hell, the retro design would generally make it modern inside and classic/retro on the outside.

other designs i loved but can't tell much about:
shirtz.cool x minecraft nether keycaps:
<img width="1200" height="1500" alt="image" src="https://github.com/user-attachments/assets/b00d4e31-eba5-4e1d-8311-fa38e3765954" />
shirtz.cool x minecraft cherry keycaps:
<img width="1200" height="1500" alt="image" src="https://github.com/user-attachments/assets/1c7975e7-ec19-486f-b69e-d785d5b5b928" />
Varmilo VA100 CYMC/Moonlight V2:

<img width="750" height="305" alt="image" src="https://github.com/user-attachments/assets/146c795c-3a66-4c0a-bff8-635f948ad9cd" />
<img width="2400" height="849" alt="image" src="https://github.com/user-attachments/assets/56959f81-feb7-4e35-9332-117aba1dcedc" />
HM: teenage engineering inspired vibe and style:
<img width="985" height="352" alt="image" src="https://github.com/user-attachments/assets/8e8fe719-5709-46b8-8ecb-569404f45133" />


## 30.07.2026 - EST time: `3 hrs 41 min`
> KiCad basics && design refining

I was pretty unfamiliar with the KiCad app, well i "worked" on it one time but it was more of a larp, before making the final matrix i decided to play around in KiCad and refine the design

<img width="633" height="592" alt="image" src="https://github.com/user-attachments/assets/12e65f15-d316-4994-aea9-077bc758a239" />

Apparently KiCad isn't that hard to learn, i even started making the sketch of the matrix but, uhmmm... making a matrix for a not so aligned layout (aka the standard ANSI)

<img width="403" height="846" alt="image" src="https://github.com/user-attachments/assets/52e29fec-730e-492c-9191-51be0d552962" />

with the help of [PCBGEN](https://pcbgen.herokuapp.com/) i got the rough idea of my target rows and columns

## 30.07.2026 - EST time: `3 hrs 11 min`
> refining the schematic

Before:

<img width="1472" height="436" alt="image" src="https://github.com/user-attachments/assets/e563e046-e32c-42d9-9ee1-b072bfda158f" />

After:

<img width="2026" height="661" alt="image" src="https://github.com/user-attachments/assets/f305c487-209f-4249-95db-a84f0c46532a" />

(PCBGEN matrix layout for reference)

<img width="1333" height="542" alt="image" src="https://github.com/user-attachments/assets/7a59f79e-b203-44af-8c18-8b9139a42c2c" />


with the help of a few guides, a reference and a few hours of hard work i managed to optimize my schematic so that it matches my initial design, also i made room for the OLED screen and connected both RotaryEncoder_Switch to the matrix! tho I'm not so sure about that, from my perspective, i wired them exactly the same as a switch (because it's essentially a switch, duh) with a diode and col2row connection, the problem is that most LLMs I asked flagged this exact decision as wrong, anyways that's a problem for later.

<img width="2029" height="1155" alt="image" src="https://github.com/user-attachments/assets/b54b15ae-889d-413a-a00f-840cdf348a96" />
finally I'm done (at least for a while) with the schematic!

## 31.07.2026 - EST time `5 hrs 12 min (!!!)`

<img width="1169" height="585" alt="image" src="https://github.com/user-attachments/assets/e8de6b77-22d1-4235-a480-74f3c571e523" />

that was... a long time, i added safety features like capacitors and rewired the LEDs, now it's time for F8 and final PCB structure 

SOME debugging later i found out that i put 1 extra switch in between "+=" and "backspace" keys (notice how there's an extra SW under the keyboard?, that was the odd one that made me rethink my design), anyways I fixed it by just drawing the whole keyboard like 3 times

<img width="1896" height="755" alt="image" src="https://github.com/user-attachments/assets/1b57249c-43f4-48d6-a064-65a177ff1bc9" />

<img width="1870" height="948" alt="image" src="https://github.com/user-attachments/assets/d5ab7175-e211-4bc3-8c8d-a1eb4cc4ae84" />

"FINAL" (aka perfect key count) version: 

<img width="1271" height="566" alt="image" src="https://github.com/user-attachments/assets/a3b93708-42f5-4e02-bee2-fa104b248aa0" />

My last commit for today, I finished 1 key and will replicate it later

<img width="776" height="710" alt="image" src="https://github.com/user-attachments/assets/4b6d0412-b421-4091-9a3f-3f58bc031fec" />

## 31.07.2026 - EST time `2 hrs 30 min`
> Recreating the design on the PCB

Finally my matrix looks like the schematic and it finally looks like my original idea! i finally reordered the dumb switches, wired them with their respective diode and LED and... it's so interesting but i'm sooooo tired of working today, at least now it looks PERFECT and I only need to add the Pi Pico (which might actually transform in a ESP32 or the RP2040 chip), MCP and wire them together.

<img width="1687" height="695" alt="image" src="https://github.com/user-attachments/assets/46d23942-00db-48d6-9e2f-4bcfe395bbdc" />

## 01.08.2026 - EST time `3 hrs 45 min`
> wiring

Soooooo i completely forgot about devlogs... anyways, since I fixed some layout problems on the PCB it's time for the most tedious process that I initially thought was automated...

<img width="1457" height="637" alt="image" src="https://github.com/user-attachments/assets/81c87c23-0753-46ee-9799-4315882b1dfb" />

<img width="1331" height="252" alt="image" src="https://github.com/user-attachments/assets/e902e7dd-4eae-40ce-9372-2984c327684e" />

since that's my firs time working and actually wiring something it's.... absolute dogshit... I mean if it works I can't complain, especially when the only thing in common between my project and the guide is that both are keyboards, the guide has all it's keys and switches in a perfect table, no LEDS and NO hotswap, also it doesn't use I2C or any GPIO extension whatsoever, wiring it is like drawing lines in a sketchbook. like no offense but IMO the guide must show the most difficult example so that the ones that don't care can ignore adding and wiring stuff. Also wiring and most things on the guide are "hit x to wire, pg up/down to go to F.Cu and B.Cu, you'll figure it out"

## 02.08.2026 - EST time: `5 hrs 1 min`
> re routing and optimization

sooooo apparently my routing sucks... that's why I had to delete every path and redo them from scratch...
I don't think I have any "before" screenshots (SIKE) but it's bad

BEFORE:

<img width="1276" height="546" alt="kicad_NXhsbIXjEU" src="https://github.com/user-attachments/assets/0a3401a4-1733-40da-ad50-6289c12b57f4" />

AFTER (another man made horror beyond anyone's comprehension):

<img width="1399" height="823" alt="image" src="https://github.com/user-attachments/assets/275dbc39-2c60-406d-bb48-e40dfcc1643f" />


That's the most efficient and beautiful I could make it, I mean it still sucks in like 10 different ways but yk, it's my first time, and if it works it works

<img width="1295" height="654" alt="image" src="https://github.com/user-attachments/assets/4ed721e5-9bee-4e70-b9d0-b61ea6838ff2" />

(GOD it's been like 25 recorded hrs and more like a week of unpaid all day labor and I'm not even done with the PCB yet... IHMAWTD)

## 03.08.2026 - EST time `3 hrs 05 min`
>finishing the rows

<img width="706" height="818" alt="image" src="https://github.com/user-attachments/assets/745a70f9-d9e7-4a1d-9425-eb62edd9c68d" />


I FINALLY finished wiring the damn rows, not that it was hard but sooooo tedious and generally until i understood how to I wasted so many tries, anyways it's done and it looks... fine? yes, it's far from perfect but have respect, it's my firs time doing something serious in kicad, I'ma be so proud if I will make this project real, genuinely a next level of flex is using a keyboard that you made all by yourself (an a bit of funding ofc).  
(this is 1/2 of today's devlogs, if I work hard I'll finish the PCB today, or at least this week). (I mean generally that's the hardest part, even though my 3D skills are not so good i think the case will be a breeze)

## 03.08.2026 - EST time: `4 hrs 45 min (!!!)`
>FINALLY I'M FREE FROM THOSE DAMN LEDS!!!!!!

<img width="2162" height="913" alt="image" src="https://github.com/user-attachments/assets/3da0f7c6-f919-4ac8-8c6a-0ffa7a5b0209" />

No extra comment, just free at last... ONLY POWER REMAINING AND THE PCB IS *LE DONE*

## 04.08.2026 - EST time ` 4 hrs 43 min`
>*LE PCB* is *LE done*

GOD I'm so tired, like it's not hard but so tedious to wire everything and the damn GND fill that only breaks my design, even though i said it's done i still have to either hand route all GNDs or make the GND fill work

<img width="1451" height="532" alt="image" src="https://github.com/user-attachments/assets/ee0854fa-bb0e-42cf-a398-a7f58308f005" />

fixed wiring, ready for filling everything

<img width="1715" height="630" alt="image" src="https://github.com/user-attachments/assets/a16e63e1-303c-4a53-8e97-e78200aac46f" />

OMG I'M SOOOOOOOOOOOOOOOOOOOOOOOOO TIRED.... the damn kicad gives me errors like "pin 1 and pin 1 are not connected" like what do you mean stupid ones and zeroes, they are one solid piece of copper!

<img width="1251" height="875" alt="image" src="https://github.com/user-attachments/assets/87b1810f-d35e-4c9a-8f19-d64fbeb4b596" />

AND I STILL GET ERRORS THAT ARE JUST RANDOM BS!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

## 05.08.2026 - EST time `4 hrs 28 min`
> FINALLLLLLLLLLYYYYYYYYYYYYYYYYYYY FINISHED THE DAMN PCB, SUCK IT KICAD AND SUCK IT DRC

Sooooo today's 4 hrs were extremely productive, I finally finished the PCB with 0!!!! DRC errors! and yes, I just checked every square mm of the board connecting every suspicious thing 
and it somehow worked!

HERE'S THE FINAL (at least as far as MK1.2A goes) DESIGN!:

<img width="2102" height="791" alt="image" src="https://github.com/user-attachments/assets/79ec4a78-77e2-493c-9bf9-a4947ea9fe80" />

also I made a THT version in case that it was mandatory (AKA MK1.2B)

<img width="2161" height="822" alt="image" src="https://github.com/user-attachments/assets/2a3d18d2-8c27-4208-9f0f-391d5a7eeaca" />

anyways i still have to make the PCB have SWAG so I'll add silkscreen things next time

## 06.08.2026 - EST time `3 hrs 35 min`
>MK1.3

another highly productive day, I finished MK1.3 for SMD and THT! now I only need to settle on a design and make the MK2 and then using MK1.3 and MK2 design the case.

MK1.3(B) THT:

<img width="2150" height="817" alt="image" src="https://github.com/user-attachments/assets/5ddaa005-f708-4141-b993-311c178e410b" />

MK1.3(A) SMD:

<img width="2166" height="884" alt="image" src="https://github.com/user-attachments/assets/65f2cf5e-abf1-4c94-9d36-a0a40ddf73b5" />

## 06.08.2026 - EST time `3 hrs`
> Onshape sucks

AFTER 3 (NOT KIDDING) PAINFUL HOURS I gave up with on shape and decided to use Fusion. Also guess what? I managed to setup Fusion, create a project, import my .step pcb and co a mathematically perfect outline in under 15 minutes (I NEVER USED FUSION IN MY LIFE) (that took 2.5 hrs in onshape to still lag like hell on earth). Kinda wasted time today but IDC, Fusion feels much more intuitive and it's blazing fast so making the case will be a breeze

Also I settled on the gasket mount since I care about feel and sound and also it doesn't require PCB side modifications (which is great since I have like 5 PCB revisions and variations and doing any changes on one means I'll have to redo all of them)

<img width="2560" height="1380" alt="image" src="https://github.com/user-attachments/assets/f56071a2-7562-4257-a7bc-ac5016545f46" />

## 07.08.2026 - EST time ` 0 hrs`

yeah, today I had a really bad and difficult day and almost got killed by a bum soooo I didn't work today at all.... shame on me

## 17.08.2026 - EST time: ` 3 hrs 44 min`

sooo today i came back from a vacation and my comeback started really productively, I finished the plate edge (with the gasket notches) and i started the hardest part of the damn plate aka the holes for the switches and other stuff... predicting to finish in 48 hrs from now

## 18.08.2026 - Est time: ` 3 hrs `
>Plate

sooo i finally finished the switches (and other stuff) overlay and from what I understood i only need to extrude them and that's it! I'm soooo happy!

<img width="1830" height="771" alt="image" src="https://github.com/user-attachments/assets/c3bdf404-1463-4a6f-9074-0be646229cfa" />

## 19.08.2026 - EST time: `3 hrs`
>plate design

Today I did the holes for stuff like the pico, USB port, stabs and other stuff that normally must not be covered by the plate. it was a pain since i had to learn fusion to do anything AND i had to invent stuff just because IDK how else am i supposed to do it. i took inspiration from my current keyboard to finish the holes.

<img width="1479" height="623" alt="image" src="https://github.com/user-attachments/assets/29e24e2f-b269-4c7a-a61f-3c96f3ed3714" />

the hole in the gasket tab issssss... kinda necessary... it looks lowk bad but IDK how else to do it

## 20.08.2026 - EST time: ` 2 hrs`
>study

today i was really tired and didn't feel like doing much so i decided to study instead. by taking a look as some other gasket mount PCBs and other DIY keebs i kinda started to understand how and why. I'm still on the "perfectionist" stage where i think everything must be mathematically correct and micrometer precise (even though half of my design is assumptions and it will be fed through a gazillion abstraction and imperfection layers anyways). I just wane my keeb to work and so that it feels good :(

## 21.08.2026 - EST time: ` 4 hrs 43 min`
>finished plate (?)

Finally i had the balls to finish the plate out of the sketches! even though it might feel easy but again, I'm a fusion noob AND my perfectionism won't leave me alone. i had to re extrude and re align it like 4-5 times before the result satisfied my needs. rn it looks like this, it's probably not the final version but it feels so good to see it in volume:

<img width="1717" height="706" alt="Fusion360_dQskucoQ7W" src="https://github.com/user-attachments/assets/e7af9762-b91a-4e50-8adb-0c9ab9e861b8" />

(also it's unrelated but i tidied my D drive and thought about switching to a smaller board to cure the tumor, it's, sadly, harder than expected and the easiest change will mean rerouting and remaking the plate and case from scratch) 

## 22-23.08.2026 - EST time: `6 hrs 31 min`

When life gives you lemons, don’t make lemonade. Make life take the lemons back! Get mad! I don’t want your damn lemons, what the hell am I supposed to do with these? Demand to see life’s manager! Make life rue the day it thought it could give Cave Johnson lemons! Do you know who I am? I’m the man who’s gonna burn your house down! With the lemons! I’m gonna get my engineers to invent a combustible lemon that burns your house down! 

<img width="674" height="323" alt="image" src="https://github.com/user-attachments/assets/62cc548a-d46d-4b7a-9c7e-b566b873aa87" />

honestly ATP idk what to do except start from scratch.

Okay I didn't give up, i just: recovered a stinky old backup; redid all the changes; redid the plate; added the screen 3d model; noticed that the screen was rotated 180 deg; flipped it in the PCB; imported the new PCB step; noticed a 1mm move; redesigned the screen hole; extruded final variant.

I'M SOOOOOOOOOOO TIRED

<img width="1288" height="562" alt="image" src="https://github.com/user-attachments/assets/fcf26ffb-93b2-46ee-aef9-91eb45575531" />

<img width="1768" height="801" alt="image" src="https://github.com/user-attachments/assets/6f97162b-f471-49fe-aea0-3a17051c14c3" />

<img width="2027" height="436" alt="image" src="https://github.com/user-attachments/assets/100a4479-bfc7-438f-ba09-babdabec39a1" />

this plate is haunting me for over a week already

## 23.08.2026 - EST time `2 hrs`
>case design

As soon as i was 70% okay with the plate i started designing the case itself, as of now i decided to make it go 9mm below the PCB, to be 4mm thick so that it overlays the tabs with 2mm and i still will be able to add clearance for the poron/silicone.

<img width="1539" height="1072" alt="image" src="https://github.com/user-attachments/assets/c4d0c7e9-5d2c-4bfd-a32e-66cff72315a4" />

this design gives me a 5mm bottom - PCB gap, perfect for a poron dampener

## 24.08.2026 - EST time `~6 hrs (4 + 2)`

Today I was working all day with a break and 2 total sessions, I finished the case skeleton and it's ready for the finishing touches! I extruded the initial walls of my bottom case, then cut out the tabs from the extrusion, since I still needed to fit the gasket and i needed some wiggle room so I made the hole 1mm wider and to fit the gasket I made it 2mm deeper (i will be using a 3mm poron sheet for the gaskets and it will be 33.(3)% compressed which is actually the perfect compression for poron. then I did the same for the upper part. Then i noticed that the case and the plate have 0(!)mm clearance, that's bad, so i pushed extra 0.2mm from the case walls to give extra room.

<img width="1245" height="504" alt="image" src="https://github.com/user-attachments/assets/6a0c9f79-52f2-4d36-b50b-35a37324a299" />

<img width="1481" height="906" alt="Fusion360_1F4rwa9MFO" src="https://github.com/user-attachments/assets/b24018ae-74d1-4048-afda-13abe3d745bf" />

<img width="1611" height="906" alt="Fusion360_Ch0pzffZ9U" src="https://github.com/user-attachments/assets/ae871591-f89f-4223-9de7-2d3ad997ffcc" />

At the end I'm more than happy with the design and it's still not the end, I still need to add cosmetic improvements and perform useless tests until I'm happy with the results and until I feel like it's production ready 

## 25.08.2026- EST time `3 hrs 22 min`

today i searched for like an hour straight to find an exact 1:1 replica of a Pi pico but with a type c port, and I found IT! it's technically a ESP C3 in the body of a pico and it's like 3mm shorter than the pico i decided to use but who cares, it works for me! That meant that my initial guess on the type C is not necessary anymore! (that also mean that I'll need to redo everything if i decide to use a THT pi but that's a problem for later) 

during hole making process the hole tool actually clipped lile 0.1mm over the upper body so instead of extruding it 1mm i added a "lip"

<img width="1369" height="322" alt="image" src="https://github.com/user-attachments/assets/a3228c9c-c718-4da5-a4d5-aceb23f8d222" />

The finished result looks PERFECT!

<img width="869" height="779" alt="image" src="https://github.com/user-attachments/assets/aeb8d5f4-c09a-42a3-93a5-9e3be30fade5" />

it will fit 99% of type c cables since i added extra clearance ++

<img width="995" height="649" alt="image" src="https://github.com/user-attachments/assets/d97bda48-98f1-4e82-91a9-9cd01733bfcd" />

<img width="1122" height="729" alt="image" src="https://github.com/user-attachments/assets/b80e65d8-6b8c-428d-83c6-7a2a8b154511" />

I think the case is 90% done, a few cosmetic modifications and I think i'm ready to ship!!

## 26.08.2026 - EST time `2 hrs 33 min`

since it's the end of my journey i spent all day fighting with fusion and JLC to export and check for manufacturing for my stuff. apparently it's cheaper than i thought. but fusion still fights back by crashing on any action. I still have to make the 2 parts meet but the guide doesn't say much about it and i'll have to guess, again

## 27.08.2026 - EST time `2 hrs 23 min`

today I wasted all day outside and came back soooo tired that i could do much, yet i solved one of the greatest problems in my project: screws

I feared them since 3 separate sources listed different specs and sized for the same M2 screws, at the end i settled to m2 dk4 flat screws, probably 7-9mm long. I will make the top hole 2.4mm which is apparently "normal" fit for a 2mm screw and for the bottom part i will be using brass inserts that from what i recall are something like 3mm in diameter so a 3mm hole or a tad smaller will do the job.

<img width="1466" height="834" alt="image" src="https://github.com/user-attachments/assets/e6e76949-bc26-484f-812d-5e6e6806b9c1" />

that's the layout I settled on because Gemini says that too much = too much and that it will distort the sound and stop natural bending or idk. i settled on screws almost every in between tab space, that's roughly 9-12 screws and i'm happy with it.


## 28.08.2026 - EST time ` 3 hrs 10 min`

for like the fifth time already life throws combustible lemons at me, this time all the switches collided just a bit with the pcb which meant that i either needed to start from scratch or get creative. Apparently getting creative got me in experiencing collateral benefit as fixing the switch placement fixed my case clearance issue almost completely!

Before:

<img width="892" height="839" alt="Fusion360_5Ro4m1fYNc" src="https://github.com/user-attachments/assets/eb47a92d-fb1e-4adb-a38f-1632b896af7a" />

After:

<img width="1135" height="1026" alt="Fusion360_odiPu61Ybg" src="https://github.com/user-attachments/assets/9c047526-50eb-4411-a283-db3127deddb2" />

now for my poron dampener to work I need either to rise the bottom like 1mm or pray that the current design is good enough (this will also mean trimming the pins but shhhh)


Also today I almost finished with screws + fixed the port hole problem

<img width="1173" height="748" alt="image" src="https://github.com/user-attachments/assets/02e350ca-a8bc-4c1c-afb3-4262eb8016be" />


## 29.08.2026 - EST time `2 hrs`

life doesn't hesitate throwing lemons at me again so i couldn't move my shetch, anyways i still have my holes so i'm okay with that

<img width="1241" height="508" alt="image" src="https://github.com/user-attachments/assets/44da7784-8f40-4e38-9ae3-9ff4beb18b30" />

<img width="431" height="748" alt="image" src="https://github.com/user-attachments/assets/666f3a8a-3faf-4a0f-9bce-04609ea6757f" /> <img width="423" height="748" alt="image" src="https://github.com/user-attachments/assets/3222db98-fad7-43f7-8157-924f0c405c7f" />


i made my holes for M2 3*3 brass inserts, the top case will be held down by the screw but without threads and apparently 2.4mm is a "normal fit" for a 2mm screw, the bottom case is getting a 2.8mm hole to fit the 3mm insert. 

also i fixed the hole since it was imperfect

Before:

<img width="1337" height="858" alt="image" src="https://github.com/user-attachments/assets/034fc5bd-359c-48b7-bac5-d7c00da33055" />  <img width="519" height="298" alt="Fusion360_aVNNW6SzFp" src="https://github.com/user-attachments/assets/835eef6a-bbaf-4a5f-9cf9-e0c05a8755a4" />

After:

<img width="1186" height="818" alt="image" src="https://github.com/user-attachments/assets/5fa32e1e-fa2c-4f51-bd34-f590b20409b4" />
