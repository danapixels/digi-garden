# Cursor Hotel Progress
Created June 8th, 2025

Cursor hotel is an MVP for a project I thought about when I visited Dimden.dev's website. I really enjoyed seeing another cursor on a webpage. We communicated by moving our cursor to the Discord link. 

I also had a similar non-verbal experience with Journey and through this project, maybe I can emulate a similar emotion with others.

Note: This is all coded with AI since I have 0 idea how to program. This will be reviewed by an actual engineer. Credits to @Mshj for helping me.

My approach to this is asking AI to generate code one requirement or functionality at a time. This might not be the best approach but it helps me feel confident and catch unintended functionality rather than asking it straight up to create something from scratch.

Goal: A place to put your cursor when you AFK.
![[promo.png]]
## Phase 1: Function
### Phase 1 features
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

	- [x] Label for name
	- [x] Label for AFK timer

### Phase 1 log

![[transparentlogo.png]]
 Clearly this is my pixel style that I like to use LOL so I decided to go with this since it's minimal, easy for me to make, and I can still be creative with constraints without making anything too complex.

This was relatively easy to do using ChatGPT and Claude, lots of copy and pasting but lots of understanding fundamental structure of React.

- Note: I don't document even HALF the bugs I encountered or I might go crazy. This is the con of vibe coding, as someone who isn't a developer or engineer. I do NOT understand logic so it's even harder to debug or understand whats happening. I made sure to use console logs and inspecting the errors coming up in the console. 
- I've definitely gotten better at triaging this. Instead of trying to spaghetti a bad prompt and work with what it sent me I would tell Cursor or whatever AI I ended up using to revert the changes, go back, and just rewrite a more specific prompt. I try to be as technical as possible (within my knowledge) for AI to understand me.

- [x] Bug: Fix hover on purple
	- [x] Possibly due to browser (It was)

### Phase 1 prompt examples
Prompt examples:
My approach is get some kind of template I can work with, I don't want AI to build the whole thing from the ground up.
- "*write a react website app where you're able to see other people's cursors*"
- AI sent me .jsx "*instead of .jsx i'm using .tsx*"
- "*can you make it so when a user moves their mouse you can see the dot and can you make it so when the user disconnects, the cursor goes away*"
- "*using my server.js can you make it so that the cursor ids are remove when disconnecting and the cursor*"
- "*can you make sure my client or server supports this functionality*"
- "*can you make sure the handler is wired correctly*"



## Phase 2: Actions
### Phase 2 features
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
### Phase 2 prompt examples
I still used ChatGPT and Claude here, I did run into a loop at points. At this point, I really pivoted to Claude, I noticed a dramatic improvement in clarity with it or maybe my prompts got better?

Prompt examples:
- "*the hearts stay on the screen, i want them to be removed after they go to 0*"
- "*thanks, there is a bug where the hearts stay on the screen if you spam click*"

### Phase 2 log
At this point, I'm running into road blocks with copy and pasting code snippets since my desired functionality is becoming very specific. I saw a Youtube video about vibe coding (I do not support vibe coding replacing actual engineers or developers) and she mentioned Cursor so I decided to change my approach and try it out.



## Phase 3: Fun
This is where moving to Cursor helped me a lot, there was a lot of complex interactions which otherwise I would not have been able to do. My plan is to move to Continued using VS Codium (for future implementations and projects) once this project MVP is completed since it's open source. Cursor has a better UI especially for someone like me LOL but I really want to finish this project so I'll stay on Cursor for now. 

### Phase 3 features
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

### Phase 3 prompt examples
You'll notice here I was able to create so much essentially because I was able to better understand how to communicate with AI. To create the panel, I would ask the AI to do make a button using x.png and the hover state is y.png inside a container with 4 containers on top of each other. Once the button was perfect I asked it to repeat it for each button.

Another con I noticed is with vibe coding, is I found myself playing with my project a lot since I wasn't sure if my spaghetti code completely broke edge cases that I previously fixed.

Prompt examples:
- "*hello can you make it so that transparentpanel.png is in a container and the container is sticky to the right side, please keep it the original size and inside could you create 4 containers on top of each other vertically. in the first container i want hatstitle.png in the first container. in the 2nd container, 1st row i want bunnybutton.png and capbutton.png, in the 2nd row i want slimebutton.png and astronautbutton.png, in the 3rd row i want beaniebutton.png and headphonesbutton.png, in the 4th row i want sproutbutton.png and catbutton.png and in the 5th row, i want the deletehatbutton.png. in the 3rd container i want the furnituretitle.png and in the 4th container 1st row, i want the chairbutton.png, lampbutton.png, and bedbutton.png, in the 2nd row i want wallsbutton.png, plant1button.png, and plant2button.png, and the 3rd row i want blackcatbutton.png, whitecatbutton.png, and deletefurniturebutton.png*"
- "*8px please and could you make it so that when a users hovers over bunnybutton.png it changes to bunnybuttonhover.png and when they click on it, it changes their cursor to bunny.png, and other users are able to see it. when they hover over capbutton.png it changes to capbuttonhover.png and when they click on it, it changes their cursor to cap.png and other users are able to see it. could you do this for everything in the 2nd container the images it should change to on hover should have "hover" in it. for the cursor it should change to it should have the first word should match the hover state and the default state. could you also put leaderboard.png underneath the logo.png with no gap between them*"
- "*could you make the hover state for chairbutton.png as chairbuttonhover.png, for lampbutton.png make it lampbuttonhover.png, for bedbutton.png make it bedbuttonhover.png, for wallsbutton.png make it wallsbuttonhover.png, for plants1button.png make it plants1buttonhover.png, for plants2button.png make it plants2buttonhover.png, for blackcatbutton.png make it blackcatbuttonhover.png, for whitecatbutton.png make it whitecatbuttonhover.png, and for deletefurniturebutton.png make it deletefurniturebuttonhover.png*"
- "*could you make it so inside the leaderboard container, the name of the person with the highest afk timer's name they inputted is there in player 2 font*"
- "*could you make it so when you press chairbuttonhover.png a chair.png spawns in the middle of the users window*"
- "*keep the chairs original .png size, it should stay spawned. if a user clicks and drags they should be able to move it around. clicking also changes deletefurniturebutton.png to furnitureselectedbutton.png, if they drag the chair over furniturehoverbutton.png it will despawn the chair.*"
- "*other users should be able to see each others chairs they spawned and new users should be able to see it similar to how they are able to see the live cursors before they connect*"
- "*it broke. the chairs should spawn in the middle of the screen, they should be clickable and draggable by everyone and everyone should be able to delete the chairs everyone should be able to see the chair even new users before they connect. these should function similar to the cursors, the position is realtime and everyone is able to see it's position even when its moving or deleted*"
### This phase never ends
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




## Phase 3.1 The dreaded canvas
These are extra bugs I ran into when turning my project into a large canvas size. After consulting with Mshj, he mentioned to me this is something engineers would determine in the beginning of the project. My ignorance thought I could just change my project to a canvas type because I'M JuSt ChAnGinG tHe SiZe oF tHe ScReEn rIgHt? Well no, because I've been building it to a certain aspect of a screen this whole time, everything needs to be reworked to account for 4000 x 4000. 

### Phase 3.1 features and bug fixes
- [ ] Set limits
	- [x] Render only visible area, store items as coordinates, and persist data as structured item 
	- [x] Moved deleting furniture to bounding box of furniture
		- [x] Fixed bounding boxes
	- [x] Fix for client should update the cursor when dragging
	- [x] When frozen on a bed or chair user's cursor should unfreeze show when move furniture
	- [ ] User is only able to spawn 100 items per connection?
	- [ ] If a user tries to spam spawn 50 items in a few seconds they will get kicked
	- [x] User is unique? Cannot open a new tab to connect more than twice
		- Not for MVP
	- [x] Should furniture despawn if a user disconnects? 
		- No, the furniture will despawn after 24 hours

### Phase 3.1 prompt examples
- Not much to say here except I was really banging my head against the wall when going to 4000 x 4000.
- I noticed AI loves to add their own UI flares unprompted.. Maybe it think you'll appreciate it for completely destroying your current functionality.
	- Which is another thing to note, I noticed ALL AI always removes my functionality. I think it's priority is efficiency and ease? Or there's some conflicts and it's easier to remove it? Not sure.

Prompt examples:
- "*can you make the canvas size 4000x4000 units and do not break any of the current functionality.*"
	- (It indeed broke my functionality.)
- "*can you please make this a 4000 x 4000 unit canvas without breaking functionality, please do not alter it visually, do not add anything visually either., keep everything how i've designed it. I just want a larger canvas*"
	- LMFAO me literally begging the AI (this was the prompt that actually worked, can't say for sure if the code is good but it worked?)
- *"is it possible for furniture persist that users place down, they will only despawn if the user hasn't logged in after 24 hours*"
- "*do we have a database to store all the furniture positions do not do anything, i just want an answer*"
	- Looking back at these I have a stern tone LOL, AI will also just try to change your whole code. Which makes sense but I was sick of it breaking and wanted to read more to understand if it got my prompt before committing. 
- "*is it possible that we can render only visible areas*"
- "*when i place a furniture, one user sees the furniture on a different z-index it should be the same*"
- "*sorry it shouldn't spawn on the users cursor, it should spawn in the middle of their screen*"
	- I don't know why I talk to it like a literal person but if AI becomes sentient one day, they can look at my logs hehe




## Phase 4.0: Launch
- [ ] Clean up code
- [ ] Code review by Mshj
- [ ] Pay for hosting service
	- [ ] Digital Ocean: 1vCPU, 1 GB RAM, 25 GB SSD



## Phase 4.1: History
- [ ] Recording of past days of AFK?
	- [ ] This is ambitious but I think this would be nice to see one day