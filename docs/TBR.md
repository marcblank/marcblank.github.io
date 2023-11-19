# Template by Reference

## Usage

If you use NINA Templates in your sequences, you'll find that **Template by Reference** is one of the most powerful features of Sequencer Powerups. In effect, they turn your Templates into something more akin to "subroutine calls" or "macros". It's easiest to show this with examples.

Let's say you have a startup Template like this that cools the camera, slews and centers the target, and runs autofocus:

![](Startup.png)


If you use this in different Template Targets or Sequences (I'll just call all of these "sequences" for simplicity), you'll have these three instructions repeated in all of them. Now let's say you've added something new to your startup procedure, like opening an automated flat cover . To update your existing sequences, you'll have to go into each one and add the new instruction. Not only is this tedious, it's also very error prone - you might make a mistake in updating some sequences, for example, or you might forget to update some sequences altogether.

With **Template by Reference**, all of this repetition goes away.  Simply add the instruction to your Sequences, and use the picker to select the Template you want to reference.  So now you have this:

![](TBR.png)

Use the arrow on the left side of the instruction to expand the **Template by Reference**.

![](TBRExpanded.png)

If I now want to update my **Startup Template** by adding an instruction for my new flat device, it might look like this:

![](NewStartup.png)

If you are using **Template by Reference** in your sequences, you will find that they are *all* using your updated version of **Startup Template**.

## How Does This Work?

To use **Template by Reference** to its fullest potential, it helps to understand how it works. And it's really very simple. The **Template by Reference** instruction simply *refers* to the specified Template by its name.

The "magic" comes when you *load* a sequence with one or more **Template by Reference** into the Advanced Sequencer; at that time, all **Template by Reference** instructions *pull in* the most recent version of the referenced Template. And at that point, the instructions become part of the sequence, and the link between the *name* of the Template and the instructions *is broken*.

This means that If you edit the contents of a **Template by Reference** that you've expanded in a sequence, those changes are *local*; they do *not* propagate to other sequences. But what if you *want* to make changes *and* have those changes be "seen" by other sequences? That's simple: just *save* the Template as you would save any other template.

Again, this all makes sense if you remember that **Template by Reference** gets the Template and its instructions *when it is loaded into the Advanced Sequencer*.

## Confused?

At first, some of this might seem confusing, though I've tried to make it comprehensible. If you have questions, please don't hesitate to ask on the #sequencer-powerups channel in the NINA Discord.