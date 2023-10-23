# Lab 31: Red-Black Tree

In this lab, we will learn how to restructure and recolor a red-black tree as keys are inserted.

Included in this project is a [red-black tree class](https://github.com/Henrik-Peters/Red-Black-Tree) by Henrik Peters. In addition to the usual red-black insertion and deletion operations, it also provides a `dumpTree` function that produces a [Graphviz](https://graphviz.org) illustration. We will use this function to visualize the state of the red-black tree.

## Part 1: In-order Insertion

Let's start with a simple example. In `main`, create a new red-black tree of integers:

	RBTree<int> tree;

Next, add integers 1 through 5 to the tree in order:

	tree.insert(1);
	tree.insert(2);
	tree.insert(3);
	tree.insert(4);
	tree.insert(5);

Can you predict the state of the tree at this point? For help, refer to the Chapter 10 slides and Figures 10.29 and 10.30 in the textbook to determine the state of the tree after each insertion. (If you are completely stumped, run a simulation using the [animation by David Galles](https://www.cs.usfca.edu/~galles/visualization/RedBlack.html).)

When you are ready with your prediction, invoke `dumpTree`:

	tree.dumpTree();

This should give you a representation of the tree in Graphviz format:

    digraph G {
    node [style=filled, penwidth=2, fontcolor=white, fontname="Arial Black"];
    graph [pad="0.1", nodesep="1", ranksep="1.5"];
    "2" [shape=circle, style=filled, fillcolor=black]
    2 -> 1
    "1" [shape=circle, style=filled, fillcolor=black]
    2 -> 4
    "4" [shape=circle, style=filled, fillcolor=black]
    4 -> 3
    "3" [shape=circle, style=filled, fillcolor="#EB0000"]
    4 -> 5
    "5" [shape=circle, style=filled, fillcolor="#EB0000"]
    }

Copy-paste the output of `dumpTree` into an online Graphviz tool such as [Edotor](https://edotor.net) to render the graph.

## Part 2: Your Own Insertion

Repeat Part 1, but instead of the numbers 1 through 5, insert any five numbers of your choosing.

Were you able to predict the final state of the red-black tree?
