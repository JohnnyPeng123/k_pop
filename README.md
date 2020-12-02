# k_pop
View this visulization from:

https://htmlpreview.github.io/?https://github.com/JohnnyPeng123/k_pop/main/index.html

![alt text](https://github.com/JohnnyPeng123/k_pop/blob/main/screen-shot.PNG?raw=true)

The implementation of the individual radial tidy tree in the visualization was based on the codes from the link below:
https://observablehq.com/@d3/radial-tidy-tree

In addition, in order to create the visualization shown in the previous page, additional modifications including data preprocessing and adding the drop-down box. 

Korean pop (K-pop) is a music genre that is originated from Korean and became popular among the young people around
the world. Typically, K-pop stars belong to a particular group, and the members of the group will write song and perform
their music together. Furthermore, these groups will belong to a particular label, these labels normally manage multiple
groups of artists at the same time and helping them to find jobs and performance opportunities. This member-grouplabel relationship forms a natural hierarchical structure, and thus I thought the Radial Tidy Tree layout would be a great
fit for the K-pop dataset.

There are Six main marks/elements in this visualization:
1. Drop-down box at top left corner – This feature allows the user to view the label that they are interested the most.

2. Roots – This is the nodes at the centre of the radial tree, it represents the selected label.

3. Nodes in the first Layer – These are the nodes that is one layer away from roots, they represent the artists or Kpop groups or managed by selected label. Note that, all the artists in this layer are the ones that does not belongs to any other K-pop group.

4. Nodes in the second Layer/Leaves – These are the nodes that is two layers away from roots, they represent the
individual K-pop groups members. They are the children of the K-pop groups which they belong to.

5. Links/Edges – Since the visualization is a tree layout, the edges represent the hierarchical relationship between
two nodes, and the nodes that are closer to the root would be in the higher position of the hierarchy.

6. Texts – These are the name of the label/group/artist represented by the nodes.
For example, the label of interest in the visualization from the previous page is “S.M. Entertainment”, this label was chosen
for demonstration purpose as it has the highest degree in the given data. This visualization indicates that “Red Velvet” is
the one of the K-pop group that is managed by the label “S.M. Entertainment”, and their members are “Bae Irene”, “Irene”,
“Seulgi”, and “Wendy”. If you are familiar with this group, you will notice that “Bae Irene” and “Irene” are the same person,
and two group member “Joy” and “Yeri” are missing. To be clear, this is a data issue from the given dataset rather than a
problem of implementation of the visualization, and there are more than one data issues like this exist in the given dataset,
so I did not try to make any remediation for such problem.

# Self-evaluation
• (Strength) For any selected label, this visualization can show a lot of information at a very granular level, and it is
able to answers questions relating to a specific label very well:

o Who are artists managed by label X? What are the groups managed by label X and who are the members
within each group? Which group is the largest group managed by label X?

• (Strength) As the underlying tree draw algorithm is the tidy tree drawing algorithm, which makes the graph
aesthetically pleasing.

• (Weakness) In the original dataset, the edges do not always imply hierarchical relationship. For example,
sometimes group-to-artist relationship can simply imply the group had collaborations with the artist. Thus, this
visualization representation might have misrepresented the information given by the original dataset.

• (Weakness) Not all the given information was presented in this visualization, for example this visualization
omitted a lot of non-hierarchical relationship/edges, thus this visualization cannot answer following questions:

o Which label is the most influential label (by degree)? Which the company/group isthe artist X belongs to?
Which artist/group had the most collaboration with other artists/groups?

• (Weakness) Some of the texts are displayed vertically or almost vertically, which are hard to read.
