![[launch.png]]

I will be recording the launch of iamafk.dev! Just to make note of the cursors afking on a day-to-day and to see if anything interesting happens.
## Day 1
Launch! Did a bunch of testing with Mshj before sending the link to my friends to test.
![[day1.gif]]

Everyone was really excited and spamming emotes, moving their cursors around wildly. This caused a lot of lag LOL. I asked Cursor to add optimizations for rendering and throttling the furniture since the real-time positions are broadcasted to everyone. I'll need to test this further to see how I can reduce lag for everyone.

Lots of users liked using the plants to either make art or communicate a message.

![[pride.png]]

## Day 2

![[cat.gif]]
I thought it was cute that users sitting next to their significant others or friends :D

Today users spent time making a lot of things and we experienced our first server crash today LOL. I'm not actually sure what caused it but I will try to implement safeguards today. 

Testing with a bunch of users also helped me see a bunch of QOL bugs and a huge time accumulation bug that was essentially giving everyone 60x the amount of AFK balance. 

Witnessing a win :D I like that everyone will celebrate because I've made it a community event where everyone gets the unlock.
![[win.gif]]

### User feedback implemented
- Make afk timer label easier to read (My friend Dev wanted this to be easier to read)
	- Won't implement this yet since not many people asked for this yet
- Change character limit to 50
- Furniture spawning unclear 
	- Furniture should spawn selected
- Too many emote spamming, added throttling and delay between them
 - Ban bad names from being used in usernames and added error dialog to let users know to try again
 - Removed unique identifiers from showing on client side
 -  Gacha machine label should be by the machine
 - Fast mouse causing desync? Tried a fix for this but we'll see if this works
 - CPU usage spikes to 90%, tried a fix to stop React rendering static items
- ContextAPI implementation: Prompt: For localstorage.tsx, users are manipulating data in localstorage can we implement server side validation and context api)
- Cursor statue for leader board instead, too long.
	- Leaderboard refreshes per session (all time vs daily) and shows time

Fun things to add:
- Dog, Computer, TV
- Badges for jackpot and longest historical AFK. Requested by Louis.
- More hats: loading cursor, transparent cursor, FFR cursor, and balloon cursor
- Update buttons for these new items
- Update panel to accommodate for these new items
- Create another gacha machine for furniture
- Update logo so there's no misleading drop down icon
- Change gacha banner changes name based on newest winner
- Time accumulation bug fix
- Make sure jackpot statue logic is correct
- Server used just to validate AFK time
- Later on: 
	- Furniture mechanic change
	- Mini game is bet with another person the color of the card, white or black. 
	- Raining umbrella hat
	- Music headphone hat
	- Helicopter hat
	- Guinea pig animated
	- Tea, coffee, soda
	- Double bed connection
	- Presets to save furniture selection
## Day 3

![[andy.gif]]
Again with the art using furniture LOL. Really says a lot about the human condition and needing to communicate in a non-verbal space.

![[andybuilding.gif]]

![[everyoneafk.gif]]

## Day 4

Noticed a cool building was made! (I think by Connor). 
![[connor.gif]]

5-6 daily average users :D
![[day3.png]]

Not a lot of users use the rest of the space on the canvas is what I noticed. I was thinking of creating environments to get users interested in moving beyond. But maybe if there's more users in general, they will be more likely to spread out.

Wasn't on much today was taking a break trying to finish the 1.1 update!! Hopefully, I can take a break from iamafk for a bit to focus on other things LOL. It's been burning me out.

Not much to keep people on since there's only one unlockable right now. This update will add on 4 new hats and 5 new furnitures.

## Day 5
I have about 4 consistent users without officially launching. When I do the new update I'll ask my friends to get on so I can pressure test the server. Dee won her first gacha win today. 
![[po.gif]]
Paul created his first building.
![[day5.gif]]
Such a bad bug, time accumulation is hard to fix when you don't understand what you're writing LOL. I constantly ask Cursor to double check not sure if I have it right.

## Day 6
Not much to report today, everyone afking! Like intended...

![[day6.gif]]
## Day 7 and beyond
Last update!!! I added two environments, a snow environment and a beach one. I ended up keeping the beach one. 
![[day7.gif]]
Animated wins are a hit. People love the gacha-only-accessible hats and furniture that are animated or interactive.
![[gachawins.gif]]

Someone's cool building of a lifeguard post using the furniture available to them :D
![[lifeguard.png]]

My last update until I take a break is adding presets for furniture! If a user built something complex, they take a break, and the server cleans it up then they can place it down. Or if they like someone else's work, they can duplicate it and place it down for their own use!

![[madatlosing.gif]]

I noticed what I really liked is feeling like you're with your friends all the time. Sometimes you'll catch your friends out of afk and you can greet them like seeing your friend log on in a classic MMO. 

![[day8.gif]]
## After thoughts
I learned a lot about deploying a website, user feedback from live users, dealing with crashes, the anxiety, and the joy of someone using what I created! 

This was meant to be a silly fun thing. It turned out to be something I really want to continue to push to others. Not for clout LMAO just to create a small community! It's nice to know someone is there no matter what. And it's a real person. 

I really do hope others fork my project and make their own iterations using their own art to see what kind of afk environments they make with their friends. 