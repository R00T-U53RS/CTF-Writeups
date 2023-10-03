Flag Format : iitbCTF{}

# Miscellaneous

### Find find !! (200 Points)

Nilabha bought a new processor and was comparing its performance using Cinebench, some problem happened, and the image did not render properly. Figure out which processor Nilabha was testing.

#### Solution

- Converted the given QR into black and manually created the third square corner.
- Then use [QrazyBox](https://merri.cx/qrazybox/) to analyze and extract QR information.
- Flag is in the QR info.

### Banarasi Paan (500 Points)

Greetings, Chief Deputy Hacker of THO (The Hacker Organisation)! Your relentless pursuit of India's notorious hacker, known as "Sasta Natwarlal," has led you to a critical breakthrough. Though he managed to evade capture, you have uncovered a tantalizing clue that could finally bring him to justice.

Inside his abandoned hideout, you discovered a lone USB drive boldly labeled "Catch me if you can." Sasta Natwarlal's arrogance knows no bounds, but it's also his Achilles' heel. Upon connecting the drive, you find just a single text file named "Banarasi_Paan.txt." The hacker, it seems, loves a challenge.

#### Solution

- Given text file has brainfuck language which gives a link [here](https://urlzs.com/FbD4S).
- This link has a Binary Sequence in the form of letters which are varying from each other by a difference of 1, giving Coordinates of Paan Bhandar.
- Mishra is the first name of the Paan Bhandar.
- Now we have mishra as our KEY to decode [this link](tblwj://rn.oq/1cpub) (another Link of a file).
- This link has a pcap file which on Wireshark gives another sequence to decode.
- Text1(hp/./o)Q
- Text2(ts/lSc)v
- Text3(t:tyKZ)F
- Reading from top to bottom, the link is [here](https://t.ly/SKocZ).
- Used Cipher identifier on [dcode.fr](https://www.dcode.fr) and it was binary to morse, giving the FLAG!

# Web Exploitation

### Spiderman Stuck in Web Part 1/3 (50 Points)

Help spiderman navigate across the web spiderverse!!  
LINK : iitbctf.centralindia.cloudapp.azure.com:8080

#### Solution

- `invisible.txt` has whitespace cipher which has username - gwenstacy and password - savedad65.
- On Login we have a photo either you can guess that the photo is of Mumbattan from Earth 50101 if you have watched Spider-Man: Across the Spider-Verse (2023).
- Or you can see sources in inspect which shows that on changing the url numbers we can traverse 3 directories.
- Now on this new page, you have `vision.java` file; upon reversing the code, GOT the first flag.

### Spiderman Stuck in Web Part 2/3 (100 Points)

Continue helping spiderman navigate across the web spiderverse!!  
LINK : iitbctf.centralindia.cloudapp.azure.com:8080

#### Solution

- For this part, [this page](http://iitbctf.centralindia.cloudapp.azure.com:8080/earth-50101) has a key and cipher text decode and get another username - miguelohara and password - mighty2099.
- On this page, you see a text file which has a base 32 ciphertext sequence decode and HERE is the second flag.

### Spiderman Stuck in Web Part 3/3 (200 Points)

Finish helping spiderman navigate across the web spiderverse!!  
LINK : iitbctf.centralindia.cloudapp.azure.com:8080

#### Solution

- Earth928.js Source file has (Inspect):
  ```javascript
  const message = "usernameishobiebrownpasswordiscoolpunk138";
  ```
  user - hobiebrown;
  pass - coolpunk138;

Decode this sequence from the Miles Morales : Chapters 1 and 2 by Jason Reynolds  
Page No., Line No., Word No., Character No.  
15 6 3 2  
27 10 2 1  
7 1 1 4  
33 2 3 1  
23 27 1 1  
8 29 7 1  
8 25 1 1  
{27 4 1 1  
13 4 8 2  
29 1 3 3  
17 6 2 6  
21 4 9 1  
25 2 1 2  
21 23 7 1  
10 11 9 6  
5 18 2 4  
19 1 4 3  
18 3 1 1  
18 6 10 3  
1 10 9 6  
17 2 1 4  
27 5 8 1  
11 6 7 1  
32 25 8 7  
18 2 2 1}  
flag = iitbCTF{HeremiLeeiSprowleR}

# Puzzle

### कटप्पायदी बाहुबली को .. ? (300 Points)

कटप्पायदी बाहुबली को .. ?

In another version of the story when modern age Amarendra Bahubali is being tested by DevaSena v.2

Bahu has some help though. Kattappa is there with him. However, Bahubali was doubtful as always how much value his company will add knowing this time DevaSena has not set up something for their muscle power. They are locked in a big mansion. The main door is 11 lettter combination pad-lock with Kuntal samrajya’s Flag printed on it. Getting the right combination of English letters on the pad lock will help them get out and move to the next set of challenges.

All bull like efforts of Kattappa goes waste. However, in one room - they stumble upon a something interesting. It is a circular tablet with an inscription “शृङ्गाणि च रामः पर्वकाले” The other side is not completely readable but Amarendra notices it having another three letter word followed by तु रामः पर्वकाले” Katappa being katappa bites it and is about to throw it away but Amarendra keeps it with him. As they search a bit more - they find another tablet with a hole this time. However the inscription on it says “हरिहये दुःखादपि सुखं”

Is this some clue? Are these two things related? They get baffled and Bahubali asks Katappa to go and find all tablets. While Katappa comes back empty handed, in the meantime Amarendra has found that the two tablets fit into each other. And the “hole” looks like english letter “i”. They also notice that in small letters MDCCXLVIII is inscribed near the perimeter when the two circular plates face each other.

Katappa tries to open this - but the two plates have got locked themselves. Frustrated he throws it at the wall and it breaks. Amarendra starts cursing himself to bring this guy along. However, to his surprise the surface of one of the plates when broken reveals a chit with a message that says E30V12. Now Amarendra has to understand what it represents and get to the key for the flag lock by using L33tspeak (https://www.robertecker.com/hp/research/leet-converter.php?lang=en - advanced leet).कटप्पायदी बाहुबली को .. ?

In another version of the story when modern age Amarendra Bahubali is being tested by DevaSena v.2

Bahu has some help though. Kattappa is there with him. However, Bahubali was doubtful as always how much value his company will add knowing this time DevaSena has not set up something for their muscle power. They are locked in a big mansion. The main door is 11 lettter combination pad-lock with Kuntal samrajya’s Flag printed on it. Getting the right combination of English letters on the pad lock will help them get out and move to the next set of challenges.

All bull like efforts of Kattappa goes waste. However, in one room - they stumble upon a something interesting. It is a circular tablet with an inscription “शृङ्गाणि च रामः पर्वकाले” The other side is not completely readable but Amarendra notices it having another three letter word followed by तु रामः पर्वकाले” Katappa being katappa bites it and is about to throw it away but Amarendra keeps it with him. As they search a bit more - they find another tablet with a hole this time. However the inscription on it says “हरिहये दुःखादपि सुखं”

Is this some clue? Are these two things related? They get baffled and Bahubali asks Katappa to go and find all tablets. While Katappa comes back empty handed, in the meantime Amarendra has found that the two tablets fit into each other. And the “hole” looks like english letter “i”. They also notice that in small letters MDCCXLVIII is inscribed near the perimeter when the two circular plates face each other.

Katappa tries to open this - but the two plates have got locked themselves. Frustrated he throws it at the wall and it breaks. Amarendra starts cursing himself to bring this guy along. However, to his surprise the surface of one of the plates when broken reveals a chit with a message that says E30V12. Now Amarendra has to understand what it represents and get to the key for the flag lock by using L33tspeak (https://www.robertecker.com/hp/research/leet-converter.php?lang=en - advanced leet).

HINT : You need to find the 11-letter combination, put them all in lowercase, and then encode them as "advanced leet" using the tool at (https://www.robertecker.com/hp/research/leet-converter.php?lang=en - advanced leet). Then, wrap up the resulting answer in iitbCTF{...} and submit.

#### Solution

I could not solve this one only I could get this far...  
11 letter key combination  
Kuntal samrajya’s Flag printed on it  
MDCCXLVIII = 1748 = 1ta8  
E30V12  
i
