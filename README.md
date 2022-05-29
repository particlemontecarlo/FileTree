# FileTree
```
Dependencies: treelib, os
```
Extension of treelib to provide handy utilities for making directories with ML/data science experiments in mind.
Two ways of creating trees
1. 'node view' this has finer control of appending to the tree (termed *unique node tree*)
1. 'product view' this includes list of lists - each list is created in sublevel of element of higher level list (termed *product tree*). For example if inputting a list of lists `[[a,b],[C,D]]` we would expect the following tree 

```
root
├── a
│   ├── C
│   └── D
└── b
    ├── C
    └── D
```

The latter may for example capture different values of tuning parameters that are then organised into a tree hierarchy.

The package can create directories to disk after designing the tree.
It is then possible to filter paths based on keywords.
The user may wish to, for example, organise higher level directories according to a timestamp.

#### Additional details
Tree data structure recap:
1. Each node is assigned a unique `identifier`. Used when adding a child node to a parent.
1. Node data -- in this case carrying the name of a folder -- is stored in the node `tag` property

See https://treelib.readthedocs.io/en/latest/ for more details.