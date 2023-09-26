## Project ideas

In general, we encourage students to conceive and develop their own projects.
We do however appreciate that inspiration can be a fickle misstress and hence
provide some project ideas - just in case. These are meant as seeds which you
can develop into something of your own.

### Project 1: Modelling the antennal lobe (easy)
The antennal lobe (AL) is the first order processing center for olfactory sensory
information. Sensory axon terminate in one of 51 olfactory glomeruli
(+ 7 thermo/hygrosensory glomeruli). Each glomerulus is targeted by sensory
neurons expressing a single (olfactory) receptor - some are very specific to
certain odours (e.g. DA1), some are broadly activated (e.g. DM1).

For each glomerulus there is at least one uniglomerular project neuron that
projects to higher brain centers (i.e. the lateral horn and the mushroom body
calyx). In addition, there are a number of project neurons that sample from
multiple glomeruli. Local neurons (ALLNs) are typically inhibitory (GABAergic)
and provide e.g. lateral inhibition between glomeruli.

For this project we propose you attempt modelling the signal processing performed
in the antennal lobe such as denoising and normalization.

### Project 2: Reading out long term memory (hard)

Flies can learn to associate odors with reward or punishment. Memories are
formed & stored in the mushroom body: this structure is common to all insects
and consists of parallel axonal fibers from Kenyon Cells (KCs) which target
Mushroom Body Output Neurons (MBONS).

Broadly speaking, most MBONs encode for either approach or avoidance.
Dopaminergic neurons function as reward/punishment coincidence detector they
modulate the synaptic strength between KCs and MBONs. When such short-term memory
transitions into long-term storage we expect to see actual anatomical changes,
i.e. more or less synapses between KCs and a given MBON.

![schematic of the insect mushroom body](https://onlinelibrary.wiley.com/cms/asset/fb469ee2-7560-48eb-a79c-cfcc0dd688f1/gbb12567-fig-0002-m.jpg)

Given that there is an anatomical correlate for long-term memories, we should be
able to read out a fly's memory trace by modelling its mushroom body and apply
fictive olfactory stimuli.

In particular, we propose to compare the mushroom bodies from two connectomes:

1. [FAFB/FlyWire](https://codex.flywire.ai/)
2. [hemibrain](https://neuprint.janelia.org/)

The general idea is to model the mushroom bodies using the respective
connectome's data. We will then generate activity in olfactory projection
neurons matching a range of odours (using e.g. the [DoOR](https://neuro.uni-konstanz.de/DoOR/default.html)
database) and then read-out the responses in MBONs with known valence.


### Project 3: Exploring cell types (medium)

Grouping neurons into types is useful because it simplifies the graph. In flies,
cell types are typically based on morphology (sometimes combined with connectivity).
The assumption then is that neurons of the same cell type show effectively the
same activity.

For this project we propose to use the olfactory system (antennal lobe
+ lateral horn) test this assumption in various ways:

1. By correlating the responses of neurons from the same cell type to various
   fictive stimuli, you could try to find a set of stimuli where cells of the
   same type start responding differently.
2. Why bother having more than one cell per type? For example, there are 7-8
   olfactory projection neurons for the pheromone-responsive DA1 glomerulus.
   Why so many? One possibility is that they perform some form of
   denoising/whitening so that the activity that eventually reaches the
   lateral horn has a high signal-to-noise ratio.
3. Can we turn cell typing on its head and group neurons by their activity
   patterns? Generate a model of the whole brain and throw various fictive
   stimuli at it. Then use the combined activity vectors to find neurons that
   show very similar responses - do these correlate with known cell types? If
   this works, it could serve as one-shot cell typing.



