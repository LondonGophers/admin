# London Gophers Raffles

We run raffles for lots of different prizes, e.g. JetBrains licenses, free tickets to conferences etc.  The raffle is
Twitter-based, i.e. people need to be signed up to Twitter in order to enter.

Entering the raffle works as follows:

- We announce a special code (typically one that is easy to read and then write) on our main slide deck during a meetup
- People then visit the advertised web link, e.g. [https://gophers.london/raffle](https://gophers.london/raffle) for the JetBrains raffle to enter
- They are asked to first follow LondonGophers on Twitter
- They enter their Twitter handle and the secret code
- They click “Prepare Tweet” which launches a separate window with a pre-preared tweet. This prepared tweet is something like the following:

```
Hey @LondonGophers, please enter me into the @jetbrains raffle! 5f2fe6d8dde1e4c21770b3300ce09b5143b763ddf14632588e1f22c588a7643a #LondonGophers
```

- The hex “code” in this tweet is a sha256 sum of the user’s twitter handle and the code. The remainder of the message is configurable in the page hosting the entry form
- The user clicks “Tweet” and that is their entry complete
- Only entries received during the time of the meetup (typically 19:00-21:00) count
- Each raffle is a separate host webpage, e.g. [https://gophers.london/raffle/](https://gophers.london/raffle/) for the London Gophers JetBrains raffle
- The host webpage embeds an iframe that is the raffle GopherJS application. This embedding is parameterised by a couple of parameters, including the message that the user will tweet along with the sha256 hash. More details can be found in the GitHub repo: https://github.com/LondonGophers/raffle
- The second half of the raffle is therefore the checking of the entries

Notice that setting up and running a raffle simply requies the organiser to have a Twitter account, `@LondonGophers` in
our case. Drawing the raffle (i.e. checking for winners) requires the organiser to have a Twitter _Developer_ account.
The [wiki for the `checker` app](https://github.com/LondonGophers/raffle/wiki/checker-Twitter-credentials) explains how
to setup a developer account and create the `checker` app instance in the Developer account. It is assumed from this
point onwards that you have a developer account and that you can access the credentials for the `checker` app.

Access the credentials for your Twitter app:

- Sign in to https://developer.twitter.com/
- In the top right hand corner, hover over your Twitter handle and a menu will appear
- Select "Apps"
- In the list of apps that appears, click "Details" next to your raffle checker app
- Select the "Keys and tokens" tab to see the required credentials (API secret key, Access token, Access token secret)

Drawing the raffle works as follows:

- The checker app is hosted on GitHub: [https://github.com/LondonGophers/raffle/tree/master/checker](https://github.com/LondonGophers/raffle/tree/master/checker)
- It requires a Twitter developer account to use Twitter APIs. More details in the wiki: [https://github.com/LondonGophers/raffle/wiki/checker-Twitter-credentials](https://github.com/LondonGophers/raffle/wiki/checker-Twitter-credentials)
- The README for the checker app ([https://github.com/LondonGophers/raffle/blob/master/checker/README.md](https://github.com/LondonGophers/raffle/blob/master/checker/README.md)) gives all the details of required parameters, e.g. start and end time, special code, tweet text to match etc
- For example, the following command was used to check entrants for the November 2019 London Gophers event:

```
checker -twitter -key 1.1.1.1 -start "20 Nov 2019 19:00" -end "20 Nov 2019 21:00"`
```

See `checker -help` or [the README](https://github.com/LondonGophers/raffle/blob/master/checker/README.md) for more
details on flags/options.

Because entry to the raffle is only parameterised by time of entry and the special code, the same host webpage/raffle instance can be reused over and over again. For example, [https://gophers.london/raffle](https://gophers.london/raffle) is reused for each London Gophers meetup - no changes are required in either the entry GopherJS app. Similarly, because the checker app is similarly parameterised, there are no changes there either. This also means that other organisations can use the entry and checker apps with no forking/intervention required

A raffle is drawn (winners decided) as follows:

- Find the email from the last day of the previous month which will have the licenses attached. Subject will be: “Your coupons for free licenses under JetBrains User Group Support Program”
- The number of prizes is assumed to be N for what follows
- Create entries in [https://docs.google.com/spreadsheets/d/1pTpWFHhEnVt1gsbXHscW5yBV3PtaitMxcKvqKjT8uIM/edit#gid=0](https://docs.google.com/spreadsheets/d/1pTpWFHhEnVt1gsbXHscW5yBV3PtaitMxcKvqKjT8uIM/edit#gid=0) for each of the prizes. Use unique identifiers for each prize, e.g. JetBrains code
- First run the checker app with a number M significantly greater than N. This will produce a random list of winners’ Twitter handles
- Starting from the top, send a DM to the first N winners using the following template:

```
Congratulations! You won a JetBrains IDE license! Please email glug-organisers@googlegroups.com with your Twitter handle and screenshot of this message to claim your prize!
```

- People will need to have followed LondonGophers for us to be able to DM them. If they haven’t followed us, “draw a line” through their name and move on to the next winner
- For each person you DM, put their Twitter handle in the winners spreadsheet
- When people reply, add their name to the spreadsheet then reply using the following template


```
Hi ***********,



Thanks for joining us last night (**** CHECK LAST NIGHT IS CORRECT *********)!



As promised, attached is a one-year license for a JetBrains product.



You can use it for GoLand, or even for IntelliJ Ultimate which

supports the official plugin that will add the same functionalities as

GoLand.



Bear in mind that this coupon will expire if not redeemed (see

date on coupon).



These licenses have been donated by JetBrains; they kindly and very

happily support communities like London Gophers.



Please can you confirm you are happy for us to send out a tweet congratulating you as one of the winners and thanking JetBrains?



Thanks again, and we look forward to seeing you at the next event!




******* and the London Gophers Team
```

- When you have sent the response, mark “Sent” in the spreadsheet
- If someone gives us permission by way of reply to tweet about their winner, also mark this in the spreadsheet
- When all winners have replied with consent or otherwise for tweeting (and up to a maximum of 1 week after the event) send the following tweet:

```
Congratulations to XXX, YYY and ZZZ, winners of this month’s @JetBrains raffle licenses! #golang
```
