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
(this is 1/2 of todays devlogs, if I work hard I'll finish the PCB today, or at least this week). (I mean generally that's the hardest part, even though my 3D skills are not so good i think the case will be a breeze)
