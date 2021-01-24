# BlenderScripts-DazBone-Morph-Constraints
Script to constrain bones of one Daz character to copy another 

Can be used to remove bone transforms from morph targets/shapekeys so you can:
1. Animate Transitions between two characters
2. Combine morph targets/shapekeys to an object without the bone translations

Method for Animating Transitions between two characters:

Start by importing your two characters

For this example we will transition from Basic Male 8 to Arch Demon

I have removed the eyelashes from the Basic Male 8 character because the Arch Demon doesn't have them

I imported the Arch Demon first so he will be the Genesis8Male

I imported the Basic Male 8 second so he will be the Gensis8Male.001

![Imgur](https://i.imgur.com/DFUjdgS.png)

Click on the Scripting tab at the top and click New to Create a new text data block

![Imgur](https://i.imgur.com/7vbVDVr.png)

Paste the script

Change the Add_Constraints('Genisis8Male.001','Genesis8Male') to match your character

and click Run Script

![Imgur](https://i.imgur.com/Rssb5Op.png)

This will move all the bones in the 'Genesis8Male' Arch Demon character to the same location 'Genisis8Male.001' Basic Male character

Select the Genisis8Male.Shape first then CTRL select the Genesis8Male.Shape.001 second

Open the Object Data Properties panel

In the ShapeKeys area click the little down arrow and select Join as Shapes

This will add the Arch Demon shapekey (without bone transforms) to your Genesis 8 Male character

Click on the Genesis8Male Rig and go into Pose mode

![Imgur](https://i.imgur.com/FZxti1Z.png)

Hit the "a" to select all the bones

Go up to Pose - then Constraints - and Clera Pose Constraints

![Imgur](https://i.imgur.com/RYgI77L.png)

This will put the Arch Demon back to his original shape

Go into the Animation Tab at the top

It might be helpful to hide the Genesis8Male (Arch Demon) shape and rig

Make sure the Timeline scrubber is set at the beginning of the timeline

Click on the Genesis8Male.001 Rig

Press "a" to select all the bones

Right click ont the rig and Insert Keyframes

![Imgur](https://i.imgur.com/9Siv93z.png)

And choose Whole Character

![Imgur](https://i.imgur.com/lhcMP6N.png)

Go back into the Scripting Tab

Change the order of the characters
So change:
Change Add_Constraints('Genisis8Male.001','Genesis8Male')
to this:
Change Add_Constraints('Genisis8Male','Genesis8Male.001')

Run the script again

![Imgur](https://i.imgur.com/4onap2R.png)

Go back into the Animation Tab

Move the timeline scrubber up to something like frame 60

Make sure all bones are still selected

Go up to Pose - then Apply - and choose Apply Visual Transform to Pose

![Imgur](https://i.imgur.com/eB3p5cm.png)

The right click on the rig and click Insert Keyframes

And choose Whole Character

![Imgur](https://i.imgur.com/YFbVmrv.png)

Next go back up to Pose - then Constraints - and Clear Pose Constraints

![Imgur](https://i.imgur.com/YFbVmrv.png)

You should now be able to scrub the timeline to see the bones animate between the two characters

![Imgur](https://i.imgur.com/LxmiqPb.png)

To animate the morph target/shapekeys:

Change from Pose mode back into Object mode

![Imgur](https://i.imgur.com/kpUxfsW.png)

Click back on the Genesis8Male.Shape.011

Make sure the animation scrubber is back at the beginning of the timeline

In the shapekey area select the Arch Demon Shapekey (Genesis8Male.shape)

Make sure it's value is set to 0

Click the little dot to the right to Animate property

Once again move the scrubber to 60 (or where you set it before)

Change the Value to 1

![Imgur](https://i.imgur.com/YZ6GGcz.png)

And click the dot to the right again to Animate porperty

Scrubbing the timeline will now animate the bones and shapekeys together to animate from one character to another.

![Imgur](https://i.imgur.com/hHB4ohj.png)
