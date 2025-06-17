# Cursor Hotel Progress
Created June 8th, 2025

Cursor hotel is an MVP for a project I thought about when I visited Dimden.dev's website. I really enjoyed seeing another cursor on a webpage. We communicated by moving our cursor to the Discord link. 

I also had a similar non-verbal experience with Journey and through this project, maybe I can emulate a similar emotion with others.

Note: This is all coded with AI since I have 0 idea how to program. This will be reviewed by an actual engineer. Credits to @Mshj for helping me.

My approach to this is asking AI to generate code one requirement or functionality at a time. This might not be the best approach but it helps me feel confident and catch unintended functionality rather than asking it straight up to create something from scratch.

Goal: A place to put your cursor when you AFK.
![[promo.png]]
![[iamafk.webm]]
## Phase 1: Function
- [x] Set up live cursors June 9th, 2025
	- [x] Program custom names
	- [x] Program timer over cursor that indicates AFK time
	- [x] Cursor should not show until you enter a name
- [x] Create webpage UI
	- [x] Create name page
		- [x] Intro text
		- [x] Button to connect
		- [x] Enter username
	- [x] Logo
	- ![[transparentlogo.png]]
	- Clearly this is my pixel style that I like to use LOL so I decided to go with this since it's minimal, easy for me to make, and I can still be creative with constraints without making anything too complex.
	- [x] Label for name
	- [x] Label for AFK timer

This was relatively easy to do usiing ChatGPT and Claude, lots of copy and pasting but lots of understanding fundamental structure of React.

- [x] Bug: Fix hover on purple
	- [x] Possibly due to browser (It was)
## Phase 2: Actions
- [x] Set up cursor actions
- [x] Fixed bug where label and afk timer move the cursor position
	- [x] Double click is a smiley face
		- [x] Redo animation and visual
	- [x] Click shows an echo effect
		- [x] Create animation
		- Fixed bug where clicking connect would show the effect.
	- [x] AFK timer show above cursors after 1 minute (last moved)
	- [x] On drag a line shows and disappears 
		- Won't do this for MVP, might be too much with current actions.

I still used ChatGPT and Claude here, I did run into a loop at points.
## Phase 3: Fun
This is where moving to Cursor helped me a lot, there was a lot of complex interactions which otherwise I would not have been able to do. My plan is to move to Continued using VS Codium (for future implementations and projects) once this project MVP is completed since it's open source. Cursor has a better UI especially for someone like me LOL but I really want to finish this project so I'll stay on Cursor for now. 
- [x] Customize cursor
	- [x] A few hats
		- [x] space helmet, beanie, baseball cap, cat ears, sprout, headphones, bunny ears, none slime hat.
		- ![[hatssheet.png]]
- [x] UI side panel for customization and furniture
- ![[sidepanel.png]]
- [x] Add furniture
	- ![[furniture.png]]
	- [x] Ability to flip furniture and move up and down z-index
		- ![[badui.png]]
		- Bad UI decision by me, these two buttons essentially do the same thing... And makes the click target hard to click.
		- ![[newUI.png]]
		- New UI is much more straight forward.
	- [x] Chairs
		- [x] Cursor remains stationary when sitting
	- [x] Walls
	- [x] Plants 
	- [x] Lamps (Click to turn on)
		- [x] Turns on light
			- Won't do this for MVP, not sure what's a good way to do it without being annoying. 
			- I was thinking a small radius is the inverse colors but this might be too much for now.
	- [x] Delete
	- [x] Cats
	- [x] Bed
		- [x] Cursor remains stationary and has zzz over its head
- [x] Always raining (turn off rain client side) 
	- Won't do this for MVP, this feels definitely like a nice-to-have.
- [x] Leaderboard 
	- I added this last minute, whoever is gone the longest should feel rewarded for it :D

I decided to add emotes last minute, no communication isn't my goal but minimal communication. At the end of the day, this is place to rest your cursor when you're gone so I don't want to increase the scope too much of my project.

- [x] Minimal communication
	- [x] Thumbs up
	- [x] Thumbs down
	- [x] Smile face
	- [x] Sad face
	- [x] Angry face
	- [x] Blank face
	- [x] Surprised
	- [x] Exclamation point
	- [x] Point left or right
- [x] Mini onboarding graphic:
	- [x] Lets users know clicking sends an echo, double clicking sends an emote, double clicking on a bed or chair freezes their cursor, and pressing num keys sends emotes, click and dragging to move around
- [x] Determine canvas size
	- [x] Should users be able to scroll around?
		- [x] Is it fixed? 
			- Yes, for MVP after talking with fleshmonk and Mshj, they thought clicking and dragging is the most intuitive.
		- [x] Does it grow? Not for MVP.

## Phase 3.5: Launch
- [ ] Clean up code, code review by Mshj
- [ ] Pay for hosting service
	- [ ] Digital Ocean: 1vCPU, 1 GB RAM, 25 GB SSD
- [ ] Set limits
	- [ ] User is only able to spawn 100 items per connection?
	- [ ] If a user tries to spam spawn 50 items in a few seconds they will get kicked
	- [ ] User is unique? Cannot open a new tab to connect more than twice
	- [ ] Should furniture despawn if a user disconnects? 
		- No, the furniture will despawn after 24 hours

## Phase 4: History
- [ ] Recording of past days of AFK?
	- [ ] This is ambitious but I think this would be nice to see one day