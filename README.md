# forgi Library for RNA Secondary Structure Analysis #

#### Differences between this fork and the @pkerpedjiev's repo ###

This is a *brutal* port from Python2 to Python3, using 2py3 and some tweaking.
I am almost sure there are *many* issues around. If you find one of them, let me know.

#### TODO ####
- [ ] Third example not working

#### But why? ####

Give a look [here](https://pythonclock.org/)...

#### Back to the original README.md ####

Full documentation: [http://www.tbi.univie.ac.at/~thiel/forgi/](http://www.tbi.univie.ac.at/~thiel/forgi/)

##### Build the documentation #####

sphinx-build -b html doc ~/public_html/forgi

##### Installation #####

python setup.py install

##### Examples #####

* Color elements by name in a gradient and visualize a coarse-grain RNA

  >>> python examples/visualize_cg.py examples/1y26.cg --color-gradual h0,s2,m1,s0,m0,m2,s3,h1 -x --virtual-atoms --sidechain-atoms

* Create HTML code for a fornaContainer with colors according to the order of coarse grain elements provided on the commandline

  >>> python examples/ordered_elements_to_forna_colors.py examples/1y26.cg h0,s2,m1,s0,m0,m2,s3,h1

* Display an rna structure, save it to file, trim it and view it using eog

  >>> pdb_id="ideal_1_3_4_6.pdb"; python examples/visualize_pdb.py forgi/threedee/data/${pdb_id} --output /tmp/${pdb_id}.png; mogrify -trim /tmp/${pdb_id}.png; eog /tmp/${pdb_id}.png

