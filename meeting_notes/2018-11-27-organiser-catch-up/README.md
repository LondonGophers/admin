# 2018-11-26 Organiser Catch-up

Present:

* [Kat Zień](https://twitter.com/kasiazien)
* [Antonio Troina](https://twitter.com/londongopher_)
* [Dominic Green](https://twitter.com/domgreen)
* [Paul Jolly](https://twitter.com/_myitcv)

### No-shows at meetups

Like many other Meetups, London Gophers sees huge interest at sign-up time (which is fantastic), but then ~40% of those
signed up do not turn up on the day itself. We struggle to find venues that are large enough (see later discussion) and
so for now, like our favourite airlines, we over-book Meetups so that roughly the right number (i.e. the capacity of the
venue) show up on the day. This is less than ideal for many reasons, not least that it makes planning food/drinks hard.
But also because it makes it hard for those people who are on the waitlist to plan their time in advance. We had a
discussion about the problem and the various solutions:

Discussion:

* It's likely that people do this _because_ numbers are so limited; i.e, they sign-up to reserve a space in case they
  can make it (i.e. work schedule, etc allows)
* But this isn't really fair for those people who miss the signup... and then remain stuck on the wait-list
* People start changing their RSVPs on the Monday before a meetup... all the way up to 5 mins before the Meetup itself!
  Doesn't really allow for those on the waitlist to plan their time at all
* We could take names on the door?
  * Unless we actually _do_ something off the back of this, is there much point?
  * What if someone turns up who is not on the list? Could have a 10 min hold period?

Potential solutions:

* We could operate a paid approach to membership/Meetup signup
  * Is this really in the spirit of Meetups being accessible to all?
  * Won't this create a _big_ overhead in terms of organiser management, refunds?
  * Might this complicate our position with respect to being an unincorporated society? See later notes on bank account
    application
* We could delay opening signup until the Monday before the event
  * Won't this make it very hard for people to plan their time in advance? Feels like we end up penalising those people
    who _do_ plan their time in advance, which doesn't seem fair
* We could have a phased release of places? i.e. 50 one day, then 50 the next...
  * Won't this mean that people have to place two reminders in their calendar to try and signup?

None of these options are perfect.

**Decision**: continue with the current approach of:

* announce "save the dates" at previous meetups as soon as we know dates
* create a Google calendar that people can subscribe to for meetup dates
* pre-announce signup three weeks before the meetup date, signup to open two weeks before the meetup date
* regularly remind people to update their RSVP between the opening of signup and the meetup itself

Hopefully we will see better attendance rates, which will reflect in us being able to reduce our overbooking figure.

### Understanding our audience

We need to better understand:

* who are our audience?
* what experience of Go do they have?
* what topics, formats etc do people want prefer?
* what works well elsewhere?
* what dietary requirements do people have?
* ...

This is off the back of a remarkable show of hands at September 2018 London Gophers where for ~50% of those present it
was their first meetup!

**Decision**: agreed that for now we will add a couple of questions to each meetup's signup. And use Google Forms for
things like feedback on what "Foundations of Go" topics people would like to cover.

### GLUG status and bank account

We need a GLUG bank account; covering expenses out of personal accounts, costs which are refunded after the event, is
not good for:

* the individuals who foot the large bills in the first place
* good practice as far as accounting etc is concerned. Far easier to wash everything through one account which then
  serves as the authoritative source of transactions

**Decision:**

* Continue to work on draft of GLUG "constitution" so that we can become an unincorporated society
  * Open to all to join (but with rules governing behaviour)
  * No form of selection to decide who becomes a member; no joining or membership fees
  * The Organising committee will be those people responsible for helping to organise meetups and events
  * We will have an Executive Committee for the purposes of opening and maintaining a bank account and legal status.
    This will comprise at most 3 members, and requires that the following roles be filled: chairperson, treasurer,
secretary. _Note, one person can fulfil multiple roles_
* Kat to share experience from PHPSW and draft a constitution we can use to open a bank account
* Paul to open an [HSBC community
  account](https://www.business.hsbc.uk/en-gb/everyday-banking/business-accounts/charity-banking-community-account?DCSext.nav=tabordion)
(given two organisers have HSBC accounts already, should speed up the opening process). Unfortunately Monzo don't have
the right sort of account right now

### Sharing notes/experience with other (Go) Meetup organisers

Akin to a "Meetup in a can". Sharing notes/experience with and learning from other Meetup organisers will help to make
all our lives easier, especially with regards to things like:

* Meetup group status - what's "best"?
* Accounting requirements
* Best bank account to use
* etc...

Because that way we learn once, get to the "best" answer, share with others, meaning that others don't have to
potentially incur costs/time getting to the same/similar answers.

We already:

* use our [`glug-organisers`](https://groups.google.com/forum/#!forum/glug-organisers) Google Group for shared
  communication where we need history
* have an organisers' alumni Google Group to keep in touch with past GLUG organisers
* use our `glug-organisers` Slack channel for ad hoc chat
* use our Google Drive for shared documents
* use [Meetup](https://www.meetup.com/Go-London-User-Group/) to define and manage our membership and organiser meetups
* use [Twitter](https://twitter.com/LondonGophers), Slack and [YouTube](https://www.youtube.com/c/LondonGophers) to
  communicate/share with our members
* have https://gophers.london as a sign-posting website to our main channels
* use [1Password for Teams](https://1password.com/teams/) to share credentials/private details as required

But are fairly certain we can internally improve processes to:

* make some things smoother
* make it easier to get others to help organise meetups
* ...

The options we have:

* Use a single communication channel:
  * Slack does not have history for new joiners, is not easily searchable
* Use threads per speaker/venue/sponsor in Slack or Google Groups
  * Makes things less easily searchable
* Use Google Docs
  * Ability to comment/assign etc

**Decision**:

* Use GitHub (change control, versioning) for published documents - all
* Create runbooks (Kat to draft). For each we have, over the course of 2018, established very clear requirements. These
  runbooks should make it possible (in theory) for anyone to pick up where someone else left off (which is important in
case someone becomes ill, not available for whatever reason mid-organisation). We will create runbooks for
  * How to run a meetup
  * Venues - requirements, security arrangements etc
  * Speakers - requirements, how to prepare, etc
  * Sponsors - requirements, what is allowed on the evening
  * ...
* Publish a calendar of "open spots" for speakers, venues and sponsors so that people can see "oh they're still looking
  for a speaker for Feb" (for example) - Antonio
* Trial using Google Docs to maintain speaker, venue and sponsors logs (speaker log already in this format for example)
  - all
* Spring clean Google Drive - move anything vaguely "old" to an "old" directory - all
* Look to give a talk (at London Gophers?) on "How to run a meetup?" Not to say "look how good we are" but to put the
  way we do things out there as a strawman for others to say "actually, have you considered to X, Y or Z?" - Dom to work
out where the best place to do this would be
* Ensure that we copy `glug-organisers` on _all_ speaker, venue and sponsor communication, so that any one of the
  organisers can help pick things up in case the "main" contain becomes unavailable for whatever reason

### Bigger venues

If this weren't already blindingly obvious, we need bigger venues. At our peak this year, we had 250 people attend the
Monzo meetup, with 150 on the waitlist.

**Decision**: chase existing contacts with:

* Microsoft - we need someone "on the ground" in London to help facilitate this according to Brian Ketlesen
* Google - Paul to follow up with London contact; Kat to help follow up as required
* Improbable - Dom to explore whether we could use the new auditorium
* Monzo - continue to use their great new space: it's large and largely disconnected from the main offices
* Sainsburys - Dom to chase up existing contacts

### Better serving newcomers to Go/London Gophers

It has long been our goal/aim to better serve newcomers to Go/London Gophers. But we don't have a specific section of
each/any meetup dedicated to this. We had some discussion around this:

* as far as is possible, we should try and keep the meetup interesting to _everyone_ interested in Go, regardless of
  whether they are newcomers, have been to every London Gophers meetup, are compiler developers, etc. At the moment (and
we have had feedback on this point) newcomers are not sufficiently catered for
* to some extent we rely on speakers to fill this gap. If we don't have speakers who volunteer to cover
  newcomer-appropriate topics, we are a little stuck
* we need to ensure that every meetup is as interesting as possible for everyone for as long as possible. That is to
  say, it makes more sense to put newcomer-appropriate content at the beginning of the evening, ramping up throughout
the evening

**Decision:** for Dec 2018 London Gophers, trial "Foundations of Go":

* live demos/coding covering everything from "Getting started with Go + VSCode", to "Maps in action", "Defining
  methods", "Using context.Context", "Working with JSON" and much much more
* use a Google Form to get feedback on what topics people would like to see covered
* kick-off the first one/two ourselves as organisers, whilst encouraging others to come forward and "give it a Go" in
  future
* There is a wealth of material out there that we could cover, but equally we should not feel too worried about
  repeating content every now and then because we will always have new newcomers :)


### Identifying organisers at Meetups

It's important for a number of reasons to make it easy for people to identify organisers at meetups:

* safety and security
* any issues, feedback people want to give
* answer any questions
* ...

For that reason it makes sense to wear a t-shirt/similar that is "highly visible" (although probably not hi-vis!)

**Decision:** get some organiser t-shirts, and also order some for the GLUG Organisers Alumni. Antonio to choose
something suitably loud :)

### Jobs section at meetups

The jobs section (typically held just before the break at each meetup) important because:

* it helps members who might be looking for new opportunities
* it helps other members who might be looking to hire and grow their companies
* a meetup is an excellent, relaxed place to meet and talk with potential employers/colleagues etc

At the moment, the jobs section however has become a bit unwieldy. There's always a bit of running around with the mic
that goes on, some announcements are not so clear, it's often then hard to find the person who made the announcement
during the break, we do not have contact details of people/companies on screen etc.

**Decision:**

* Ask people looking to advertise jobs to tell us in advance of the meetup
* That way we can list those who will be speaking for 30 secs at the meetup in our main slide deck

### Unconf

Antonio is a _huge_ fan of this as a concept, and gave a run through of the setup at an unconference he went to
recently:

* Attendees pay an attendance fee, ranging from £10 to hundreds of pounds
* Money goes towards anything from covering costs to accommodation for the full on retreat-style unconference
* There are swim lanes with spaces for talks and a queue talks
* People free to move between spaces throughout the entire day
* The scheduling of talks happens at the start of the day in a very ad hoc manner
* Whoever comes to your talk is the right person
* Very informal, can easily switch

Notes:

* We be an entirely separate event from Meetup
* Would best be run nearer summer time

**Decision:** Antonio to lead investigation into this. Kat to share details from PHPSW who have an excellent contact who
can advise on legal structure, setup etc.



