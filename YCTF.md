# Miscellaneous

### Unchained 1 (100 Points)

"Go from hacking web to solving puzzles"  
The admin seems to have forgotten the password, so he just want you to recover by bypassing the login page.  
Good Luck!  
Challenge link: https://harsh1tarora.pythonanywhere.com/

#### Solution

- Since we know the`admin` is the username
- I tried submitting any password while Proxy was ON and there I saw how the input was sent.
- So I tried this Command Injection `"OR'1'=='1'--` and it worked I was able to login.
- used `help` to view available commands and then `flag` command to display the flag.
- Flag was `xCTF{m0r3_way_2_g0}`.

# Forensics

### Ancient GIF (250 Points)

In the midst of a bustling town square, an enigmatic GIF played on a massive screen, captivating the crowd. Little did they know, it held the key to a hidden treasure.

#### Solution

- Extracted imagges from each frame using some website online then put QR pieces together.
- Then put the third big sqaure in the QR which is important for extracting any informationo from the QR code.
- Then I used this website to extract the QR code information - [qrazybox](https://merri.cx/qrazybox/).
- This website has a tools tab which has extract QR info option which gave me a base64.
- Flag is `xCTF{f0r3n51c5_1s_qr4zy!}`.

### Death Song (300 Points)

In this haunting song, the narrator pleads with death for a reprieve, describing death as an unstoppable force that claims both the young and old, regardless of wealth or status, and portrays it as a relentless entity with power over life and the afterlife.  
Jimmy loves to write down lyrics of the songs. Find the writer of the song which relates to the above.  
Flag format: xCTF{Firstname_Lastname}  
Link: [Google drive](https://drive.google.com/file/d/1FgVnISIXjyV9Rc7rm9phZY2hXDg2GRLB/view?usp=sharing)

#### Solution

- checked the file type after extracting the zip `file 2020JimmyWilson.E01`
- OUTPUT

```javascript
2020JimmyWilson.E01: EWF/Expert Witness/EnCase image file format
```

- As these kind of files can be mounted like file systems so I made a directory and mounted the file at that directory `ewfmount 2020JimmyWilson.E01.E01 rawimage/`
- This system had a user `Jimmy` which has a file containing lyrics of the song which i searched on google and got the writer's name from wikipedia
- Flag was `xCTF{Lloyd_Chandler}`.

# Steganography

### Inception (100 Points)

My friend got inspired by Inception movie and sent this strange image. Can you discover  
what is this image about ?

#### Solution

- Use Steghide on this file and extract.
- I got a `varman.wav` file.
- Use any Spectral Analyser and you will get the flag.
- flag might not be clear try different combinations.
- Flag was `xCTF{f0t0_1n_4ud10_1n_f0t0}`.

# Cryptography

### Movie Scene (50 Points)

When storms occur in movies, lights fluctuate.

```javascript
YKKKKYYY,
	YKYYYYKK,
	YKYKYKYY,
	YKYYYKKY,
	YKKKKYKK,
	YKKKKYKY,
	YYKKYYKK,
	YKKKYYKY,
	YYKKYYYY,
	YKYKKKKK,
	YYKKYYYY,
	YKKYKKKY,
	YYKKYYKK,
	YKYKKKKK,
	YKKKKYKY,
	YYKKYYKK,
	YKKKYYKY,
	YYKKYYYY,
	YKYKKKKK,
	YYKKYYYY,
	YKKYKKKY,
	YYKKYYKK,
	YKKKKKYK;
```

#### Solution

- With the given sequence in text file i thought of binary as there are only 2 distinct characters in the sequence.
- By using substitution in Cyberchef i replaced `Y=0` and `K=1`
- Then Converted Binary to Text and got the flag.

### Twinkle Twinkle (50 Points)

Can you decipher the secret?  
6jn3vq6s46gh5tr2z76kf1gu50y6nk6a118u6w0

#### Solution

- I tried dcode.fr to identify the cipher also tried using Cyberchef but both did not work.
- Although the hint was in the name of the Challenge `Twin`kle.
- It is a `Twin Hex Cipher`. I decoded using some online Website.
- The Flag is `xCTF{Tw1n_H3x_3ncrypti0n}`

### Military Spy (100 Points)

My Indian friend is a spy in US military, he wants to send secret message to me.  
Help me decrypt his message.  
Flag format: `xCTF{SECRET_MESSAGE}`

#### Solution

- The file with the challenge was `Secret_Message.wav` which has the morse code.
- So upon decoding that morse code I got the `S3CR3T_M355AG3_F0R_YCF`.
- Flag was `xCTF{S3CR3T_M355AG3_F0R_YCF}`.

### The Enigmatic Vault (100 Points)

In the heart of the mysterious forest, a hidden vault guards ancient relics.

#### Solution

- Put this sequence in doc file inside cipher identifier on `dcode.fr`.
- JSFuck Language [](![]+[]) --> Kenny Language (Southpark) --> Base 58 --> xCTF{HiddenVaultEntranceBehindTheFalls}
- Flag was `xCTF{HiddenVaultEntranceBehindTheFalls}`.

### Fire Accident (200 Points)

In a remote village hidden within an ancient forest, a devastating fire reduced a 58 historic cottage to ruins, leaving behind a partially burned image and a cryptic message. Some of the villgeres do belive that this fire accident was because some villegers cheated while playing their anual game festival.Legends spoke of a long-guarded treasure within the cottage, now lost in the ashes.

#### Solution

- Just used the Play Fair Cipher and got the flag.
- Flag was `xCTF{N3ver_Ch3at_pl@y_Fair!}`.

# OSINT

### OSINT 1 (200 Points)

Flag is somewhere around google maps, can you pick it? It's easy lol!  
Remember, it's not the place where he lives!  
Link: https://munazir.com

HINT : Did you visit all my profiles?

#### Solution

- After visiting around the Author's profiles I came to the conclusion that Bangalore is definitely not the place as it was where he lives.
- Then after ignoring many times I looked for Fucking Moday Madrid which was the location on Author's Twitter Account.
- Got Author's Review on Google Maps  
  `Very nice place!

eENURnswNWluMV8xc19mdW4hfQ==`

- Another Base64 and Here is the flag `xCTF{05in1_1s_fun!}`

### OSINT 2 (300 Points)

My friend wrote a very bad review about the place where he studies.  
But he didn't disclose where he studies, but I just have these information:  
`7.4956,4.44544`

#### Solution

- Searched for `7.4956,4.44544` on Google
- Got on google maps and saw a university nearby as it is given that a review about `the place where he studies` is there.
- `Oduduwa University` was the Place with a review of the Author Harshit Arora.  
   `Very great here is tha hint:  
Kzc0OTU2NDQ0NTQ0`
- Base64 and here is a number I searched it on google I got a location of Avipark Mall again went to review and in the recent reviews Author has a review.  
  It's a cruel but
  `beautiful`world,
  where secrets are`rotating` around us.
  this is a hint: @Unefuvg_1210

- At first I thought that the hint is the username but the it didn't work. So I focused on the text above the hint and saw `rotating`
- Applied ROT13 and got Author's account `Harshit_1210`
- First link was of his twitter which has bio written `SHE IS THE BEAUTY AND HERE IS IN THE WEBSITE HIDDEN` also there was link to his potfolio website.
- In the above bio there was a hint `IN THE WEBSITE HIDDEN` so I viewed the source code of his portfolio.
- The Flag hidden was `xCTF{tHis_is_R03k_d3dE}`
