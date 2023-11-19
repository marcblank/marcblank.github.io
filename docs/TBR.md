# Template by Reference

## Rationale

If you use NINA Templates in your sequences, you'll find that **Template by Reference** is one of the most powerful features of Sequencer Powerups. In effect, they turn your Templates into something more akin to "subroutine calls" or "macros". It's easiest to show this with examples.

Let's say you have a startup Template like this that cools the camera, slews and centers the target, and runs autofocus:

![](Startup.png)


If you use this in different Templates, Targets, or Sequences (I'll just call all of these "sequences" for simplicity), you'll have these three instructions repeated in each of them. Now let's say you add something new to your startup procedure, like opening an automated flat cover. To update your existing sequences, you'll have to go into each one and add the new instruction. Not only is this tedious, it's also very error prone - you might make a mistake in updating some sequences, for example, or you might simply forget to update some sequences altogether.

With **Template by Reference**, all of this repetition goes away.  Simply add the instruction to your Sequences, and use the picker to select the Template you want to reference.  So now you have this:

![](TBR.png)

## Usage

When using a **Template by Reference** instruction in a sequence, you can use the arrow on the left side of the instruction to expand it.

![](TBRExpanded.png)

Let's say I now want to update my **Startup Template** by adding an instruction for my new flat device. After the simple edit, it might look like this:

![](NewStartup.png)

Now, save the Template as you usally would, by clicking on the floppy disc icon on the right side of the screen.  Having done this, and if you are using **Template by Reference** specifying **Startup Template** in other sequences, you will find that they will *all* be using the updated version of **Startup Template**.

## How Does This Work?

To use **Template by Reference** to its fullest potential, it helps to understand how it works. And it's really very simple. The **Template by Reference** instruction simply *refers* to the specified Template by its name.

The "magic" comes when you *load* a sequence with one or more **Template by Reference** into the Advanced Sequencer; at that time, all **Template by Reference** instructions *copy* in the most recent version of the referenced Template. At that point, it is exactly as though you copied the Template into your sequence, and you can edit it, save it, or just use it as is.

If you *edit* the contents of a **Template by Reference** that you've expanded in a sequence, those changes are *local*; they do *not* propagate to other sequences. But what if you *want* to make changes *and* have those changes be "seen" by other sequences? That's simple: just *save* the Template as you would save any other template.

Again, this all makes sense if you remember that **Template by Reference** *copies* the Template into your sequence *when it is loaded into the Advanced Sequencer*.

## Confused?

At first, some of this might seem confusing, though I've tried to make it comprehensible. If you have questions, please don't hesitate to ask on the #sequencer-powerups channel in the NINA Discord.

## Appendix: What are Sequences and Templates Anyway??

There is often a great deal of confusion with what is meant by a **Sequence**, as opposed to a **Template** in NINA (And then there are **Targets**, but you're on your own there).

### Templates

A NINA **Template** is an *instruction set* that you have saved with the instruction set's floppy disk button. Here are the built in types of instruction set, along with another one (Variable Star object container) that was created by a plug-in.

![](Set.png)

You can see the floppy disc icon here on the right side of the screen:

![](Save.png)

When you save an instruction set with the floppy disc button, a **Template** is created with a name you can choose. In the example above, the name of the **Template** would be named "Parallel Instruction Set" (not a very good name).

A **Template** can contain any number of instructions, instruction sets, **Templates**, and **Targets**,

![](Areas.png)

### Sequences

**Sequences** in NINA represent the entire contents of the Advanced Sequencer at any given point in time; that is, it includes the "Sequence Start Area", the "Sequence Target Area", and the "Sequence End Area".  They are loaded and saved with icons at the lower left of the Advance Sequencer.

![](SeqIcons.png)

These things are described more fully, but with some inconsistencies in terminology, at [NINA Advanced Sequencer](https://nighttime-imaging.eu/docs/develop/site/sequencer/advanced/advanced/)




