# voicetotext

This Wolfram Language code uses the AT&T speech-to-text api to translate spoken words into text.

To run this code, first you will need to sign up for a developer account at AT&T: https://developer.att.com

Next you will need to sign up with their speech-to-text api and register an application with them.

Once you are granted this access you will receive an "APP KEY" and an "APP SECRET" from AT&T.

Place the "APP KEY" in a plain text file "clientid.txt" alongside the "voicetotext.nb" notebook.

Then, place the "APP SECRET" in a plain text file "clientsecret.txt" alongside the "voicetotext.nb" notebook.

Open the "voicetotext.nb" notebook and evaluate the section "Get a new access token". This creates a plain text file called "token.txt"
which contains the access token. The access token is valid for a long period of time, so in subsequent Wolfram Language sessions just 
import that token by evaluating the section "Get an existing access token" (and skipping the "Get a new access token" section altogether).

The notebook then contains a test[] function which is a button you can click to record a sound. This sound is then translated to text
with the AT&T api and subsequently interpreted (if possible) by the Wolfram Language. For example, if you speak "population of chicago"
then the voice-to-text api will return that string "population of chicago" and the Wolfram Language interpreter will return an actual 
people count (around 2.7 million).

Sample results:

Text: Population of chicago.
Interpretation: 2722389 people

Text: Latitude of new york.
Interpretation: 40.6643 \[Degree]

Text: Calories in an apple.
Interpretation: 0.655738Cal/g

Text: Volume of lake erie.
Interpretation: 1.61741*10^13(ft)^3

Text: Gdp of russia.
Interpretation: $ 1.8606*10^12 per year

Text: Gdp of russia divided by gdp of united states.
Interpretation: 0.106814

Text: Forty two times forty two.
Interpretation: 1764

Text: Six feet plus ten inches.
Interpretation: 82in
