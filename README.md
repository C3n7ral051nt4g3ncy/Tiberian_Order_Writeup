# The Tiberian Order: Writeup
### Writeup for the Tiberian Order - Contract: Road to Nowhere (OSINT Challenge)

*This isn't a writeup about skill, as I used absolutely no skill for this Challenge, the writeup emphasizes that if you use the right tools, and are used to competing in challenges and CTF events, you can find information quite fast.*

<br>

# About The Tiberian Order

<img width="233" src="https://user-images.githubusercontent.com/104733166/188273698-4d11c2c9-6308-44f3-8374-90284693fc6b.png">


The [Tiberian Order](https://tiberianorder.com/about/) is an ancient organization that has stood the test of time. Originating from medieval Europe, her origins are unknown to anyone except her members and clientele. In the earlier days, the Tiberian Order would influence heads of state, or take on clandestine espionage work for wealthy people.

# Contract Road to Nowhere

`Special Agent K`, we’ll be needing your assistance on a geolocation matter. One of our clients, a medium sized European goverment agency, has requested we find a needle in a haystack.

Our client is involved in fighting terrorist groups in `Asia` and `Africa`. Recently, they gained access to a Dropbox account filled with map data. Most of these seem to be related to safe houses used by a terrorist organization called `“The Meercats”`. Indeed a strange name, but nontheless, they mean business.

After having located most safehouses, our client is still struggling to locate a few of them. Since the operation to take down all of these locations needs to be synchronized. There’s an urgent need to `identify them all` before the next phase can begin.

Below you find `an image` of what appears to be a `village`, with a `red marker to indicate the exact location`. It’s your assignment to `find where in the world this is`. Currently we have reason to believe this is in `Africa` or `Asia`. But, given the organizations’ widespread members, this is only a guess at this time.

Use the `coordinates` you find `as the password to open the ZIP archive`. Inside, you find the `linkfile to your Contract Card` as always. Also, we heard the number `1920` is of importance in this case…

As always. Special Agent K, the contract is yours, if you choose to accept.

`I highlighted the important information to me for this investigation.`

<br>

# This is the image provided:

<img width="433" src="https://user-images.githubusercontent.com/104733166/188274000-900168e2-fdd0-4150-89cb-566944c1dedf.jpg">

The location would be possible to find by hovering for hours in Google Earth, I have found locations like this on past Hacktoria CTFs, but there is often hidden infirmation inside images! 

# How I solved this in less than 10 minutes

My Go To Tool is [Aperi'Solve](https://www.aperisolve.com), it's a gem of a tool, and always the first one I go to for image analysis. I also solved a challenge on the 404 CTF organised by the DGSE with Aperi'Solve.

First I submitted the image, and got no results, the great thing about Aperi'Solve is that it stores who came and when, and what passwords were tried.
I saw that 1920 was tried, Aperi'Solve won't tell you if it works however! But it came back to me that the initial mission briefing said that `1920 is highly important`, which can be classed as a hint.

We can see 9 people uploaded, and common password was 1920.

<img width="933" src="https://user-images.githubusercontent.com/104733166/188274396-f9a850b8-5f17-4e55-ad1b-871a11c7657a.png">

<br>

# Resubmitting
I decided to resubmit, by enabling password. 

<br>

<img width="433" src="https://user-images.githubusercontent.com/104733166/188275398-0d64187c-b2e4-4d9d-a450-62f689f0f827.png">

<br>

Bingo! We can see a `location.txt` file hidden inside the image with StegHide (Steganography)

<img width="433" src="https://user-images.githubusercontent.com/104733166/188275400-fa1d2f66-b407-4837-917a-d0354c255dd6.png">

<br>

# Extracted .txt File

The extracted file gives the following coordinates: 20.899370,95.118041,16
*Notice the format which wouldn't be recognised by Google Maps, this also means someone trying to solve the challenge who used Google Maps to get the location would have a hard time finding the same matching coodinates.* <br>
<img width="433" src="https://user-images.githubusercontent.com/104733166/188275586-dbf7b897-7fdb-4429-b3d4-00c9949a7d5f.png">



Gmaps format has a space after the comma, so I tweaked the coordinates in order to compare the photo to check if everything matches.
These are the coord. I used in Gmaps: `20.899370, 95.118041`

Comparing image provided in the mission briefing with Google Maps:

<img width="433" src="https://user-images.githubusercontent.com/104733166/188275824-ec1e2bce-ea8f-466a-a069-dd4d09d60f3a.png">

Location: `Hnit Kyat Khwe, Myanmar, ASIA`

<br>

# Final Step
I used the coordinates found to open the encrypted zip file, there was a link: https://bit.ly/-------, the link takes us to the contract card.











