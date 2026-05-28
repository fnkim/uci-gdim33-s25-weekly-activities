# GDIM 33 In-Class Activities
## W1
### Activity 1
[Link](https://pin.it/5Da7aV4TK)


1. The patterns emerging from my inspiration sources are mostly aesthetic-related, as I am drawn to art styles and vibes. I want to make a stylized game in a cool style
2. One of my tablemates is also making a queer visual novel, which is what I am making as well. Their game is going to be kind of dark in content, which I also want to do, although I want to do something a bit more hopeful in theme.
3. My LA enjoys soulslike games, Minecraft, and Fortnite, which is his comfort game. I think although these are very different than the game I want to make for this class's project, I als enjoy games like Minecraft. I think I don't really like soulslikes because I am bad at them.

### Activity 2
Familiarize yourself with the Vertical Slice requirements.
Solidify your game idea. At this stage, focus on:
Which genre you want to use.
Your core mechanics and gameplay loop: the repeatable actions the character will take that lead them from objective to objective.
Draw a break-down of the systems in your game in terms of objects, attributes, and actions.
I suggest drawing your break-down in a Google drawingLinks to an external site..
Refer back to the slides for examples of break-downs. 
In your Devlog, attach your break-down.

1. My game idea is a visual novel. The gameplay will involve making decisions that change the story.
2. Breakdown flowchart
![Untitled drawing](https://github.com/user-attachments/assets/5537764d-bc58-4530-ac7e-44cfe381883f)


## W2
[link to push](https://github.com/UCI-GDIM33/uci-gdim33-s25-weekly-activities-GDIM33Activities/commit/4a630c85723ede07d9f75d1d6c808837489d7e5f)

## W3
### Activity 1
<img width="900" height="600" alt="breakdown (1)" src="https://github.com/user-attachments/assets/826ada3b-8548-45fe-862f-94a323135043" />


### Activity 2
1. It's good to save the event name for the explore-to-dialogue state as a Scene variable because that allows you to reference the event easily across different script machines.
2. Using the Debug.Log() node helped me understand whether transitions were firing. My first Debug.Log() in WalrusW3 played after everything on the OnMouseDown, which meant it showed the message "AHHH" each time I clicked on the walrus. However, I was able to understand that my transitions were not working because my Debug.Log() message, "transition triggered", that was supposed to print after the game state changed from explore to dialogue, didn't print. This told me that the transition itself wasn't working, not that the problem was in specifically showing the UI or anything like that.
3. The Set Cursor Lock state is not really relevant to my Vertical Slice because I do not have a free camera exploration portion of my game; it is all visual novel/dialogue.
4. The concept of a "game state" is relevant to my Vertical Slice because there will be different screens such as choice menus or dialogue menus that are meant to be interacted with differently.

## W4
### Activity 1
Currently, my build includes dialogue that you can click through, a typewriter effect, a sprite with changing expressions and fade in/out functionality, and choices that lead to different dialogue. My playtesting goal is to check whether controls (clicking/pressing space) are intuitive or not.


Team:
Landon Her, Sebastian Magana, Kaleb Reyes, Rebecca Feng, Jess Tran, and me (Frances Kim)


Playtesting notes: The clicking is intuitive, but they didn't know about the spacebar functionality. Also, it might be better to show the dialogue box still when the choices are up rather than hiding it.

### Activity 2
Assuming this activity is completed by a programmer, could a writer add more dialogue to this setup without writing any code? Why or why not?
What limit is there to the number of dialogue nodes that the writer could create without writing any code?
In your own words, describe the purpose of the "Regenerate Nodes" button.

1. Assuming this activity is completed by a programmer, it is easy for a writer to add more dialogue to this setup without coding because the dialogue is added via ScriptableObjects, making the system scalable and easy to design.
2. There is no limit to the number of dialogue nodes the writer can create without writing any code, since they can keep creating ScriptableObject assets (DialogueNodes).
3. The purpose of the "Regenerate Nodes" button is to update the node system to contain new nodes that are added via code, or removing them. It basically refreshes the system.
Bonus point:
<img width="1326" height="744" alt="image" src="https://github.com/user-attachments/assets/f9b5f820-f031-4c38-b76f-e341311c9937" />
This image shows up when you click certain options. You can drag in a new sprite to change the image for different dialogue nodes if you want!

## W5
### Activity 1

1. Implement phase 1 for the midday state of the game, a clicking minigame where you try to cut down trees before a timer runs out.
- Implement a timer that starts when entering the midday state and goes down over time. Use a Debug Log to print the timer going down.
- Create a minigame where clicking on a button whacks a tree with an axe. Use a Debug Log to print how many times you clicked.
- When the timer runs out, stop the clicking minigame and, based on how many times you whacked the trees, give a certain amount of money

3. Implement Visuals
- Show the timer and the number going down over time in the UI
- Create another UI element that shows the whack number going up
- When the timer runs out, clear the clicking button and show a UI element that shows how much money you earned

### Activity 2
Today I accomplished creating a very ugly version of the money making minigame. I have a working UI and timer, the money clicking button works and its incrementing is shown in the UI. Once the timer ends, the clicking button is removed, and the game ends and the money earned today is calculated and put on the screen. I believe I have implemented every step as outlined in activity 1.

## W6
### Activity 1
Since my Milestone 1 submission, I have added animation to the NPC character as well as different game states for the different times of day. [The link is here.](https://fnkim.itch.io/milestone-2-gdim-33) My playtesting goal is mainly about visuals, and I will ask my playtesters to evaluate the art and presentation of the game.

Playtesting notes: The visuals look good, although there is some odd sharp edges on the sprites that could be solved with anti-aliasing. There is also a sliver of the hair that parts from the head during the animation.

### Activity 2
1. The Multiply setting of the Blend node makes the resulting color darker and less saturated because it changes the color RGB values to be closer to black than the input. Since black is represented by 0, multiplying the RGB values with a number less than 1 (a color that's not pure white) makes it smaller, making it closer to black.
2. If we use Multiply to combine Alpha values, the resulting value will be more translucent than the original values since it will push the values closer to 0, which equates to a higher transparency in terms of alpha values.
3. The shader gets UV values from data from the 3D mesh and its vertexes. This can be adjusted with UV mapping to change how the textures appear on the model.
4. Yes, it sounds interesting to me, because this knowledge will allow me to create interesting visual effects through code!

## W7
### Activity 1
1. In step 2, the data for the Vertex Color node comes from the vertices of the mesh.
2. The color is blended at the edges of different regions of color because the planes between the vertices interpolate color, causing the blended effect.
3. The shiba from step 3 has less detail than the shiba rendered with the texture because vertex color interprets color data through the vertices and blends between areas, whereas mapping textures to UV maps allows detailed images to be used as textures on a mesh. Vertex color is most more useful for things that require procedural effects, for example making shaders.
4. In step 3, there is a splotch on the left hind leg, meaning the surface normals are probably messed up there.
5. You could test UV map data using a debug shader in order to see how the UV map has been unwrapped for a mesh. This could be useful to see if there are any issues with mapping a texture onto the mesh.
6. There is an error in the lighting on the back of the Shiba because the way the Shiba reacts to the light is reversed due to incorrect normal mapping.
7. We set up the blend mode to additive for the fire effect in Step 5 so that the colors would create a lightening effect on the surroundings rather than being normal overlayed colors, more similar to fire.


## W8
### Activity 1
My build has a bit more dialogue. My playtesting goal was to check for if the dialogue worked okay. https://fnkim.itch.io/milestone-2-gdim-33


My playtesters noted that the animation of the character was cool, and the main issue was that there were a couple dialogue name mismatch issues, which should not be too difficult to fix.

### Activity 2
How are we utilizing the stencil buffer- specifically the Compare Function and Pass/Fail operations for both the Outline and Cel renderer features- in Step (2) to create the outline effect?
Open the Frame Debugger after finishing Step (2). There’s an inefficiency here. One of the objects in your Scene is drawing almost the exact same thing twice. What is it, and why is it being drawn twice?
In Step (3), why do we ADD instead of MULTIPLY the results of all the different lighting sections together?
In Step (4), why does changing the Layer the Shiba is on enable and disable the outline effect? If you’re not sure, look back on Step (4).


1. We are utilizing the stencil buffer in Step 2 to create the outline effect by checking if the value is not equal to the information from the stencil. Depending on whether it passes or fails the value check, it will either draw the color or not draw the color. In the stencil check, it either replaces the value (changing it from 0 to 1) when it Passes, or leaves the value as 1 when it fails.
2. The inifficiency in the Frame Debugger is caused by when the Shiba is being drawn twice. This is happening so that the outline effect works, which can be fixed with GPU instancing and optimization.
3. In Step 3, we ADD the results of the lighting sections together so that the shadowed section and the lit section are both drawn to the screen in separate sections. Multiply would cause each section to affect the other's color.
4. In Step 4, changing the layer the Shiba is on enables and disables the outline effect because the outline effect only affects the "Outline" layer. Switching the Shiba's layer to "Default" means the effect does not affect it.


# W9
### Activity 1
The game my team chose was Red Dead Redemption 2, particularly during the Dead Eye aiming gameplay.
<img width="569" height="322" alt="image" src="https://github.com/user-attachments/assets/8d54ae3a-a74c-47c2-aae6-93bc023f85f6" />

1. When the Dead Eye effect is initially activated via a button, there is an effect that affects the full screen, decreasing saturation, adding a vignette effect, and increasing bloom. This would likely be a post-processing effect, with the render effects being applied in a later pass.
2. During the duration of this effect, aiming at a shootable object/NPC will cause red Xs to appear on the targeted areas. This is likely activated by triggering some kind of animation that displays the symbol at the correct location.

### Activity 2
<img width="934" height="621" alt="image" src="https://github.com/user-attachments/assets/7f15e4f0-c821-41e7-9bd4-01af85b25896" />
This is the image of the Shader Graph I am currently working on. One issue I had was trying to figure out how to make the vignette effect flash on the screen. I managed to do this by adding a gradient noise and multiplying it with the texture, inputting a time node to the gradient noise's UV. After multiplying that into the final shader, I was able to creaate an effect that flashes erratically over time on the screen!
