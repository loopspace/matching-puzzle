# Matching Puzzle in TikZ

This is a little library for making a matching puzzle out of TikZ.  At
present, it just has a 24 piece hexagonal shape but more are planned.  Each
tile is an equilateral triangle, and they fit together by matching
equivalent sides.

## Usage

In your preamble:

~~~
\usetikzlibrary{matchingpuzzle}
~~~

To specify the matching sides, use:

~~~
\AddSlide{<first>}{<second>}
~~~

The hexagon shape uses 30 sides.

To show the current list of sides, use

~~~
\ShowSides
~~~

and to show the solution, use the pic `jigsaw hexagon solution`.

To produce the puzzle pieces for cutting out, use the pics:

~~~
jigsaw hexagon puzzle 1
jigsaw hexagon puzzle 2
jigsaw hexagon puzzle 3
~~~

Each has 8 triangles.

There are two shuffles that should happen when producing a puzzle.  At
some point, the sides should be shuffled.  Then the pieces should be
shuffled.

The sides should be shuffled before creating the puzzle.  It is
probably most useful to shuffle them *after* using `\ShowSlides` but
it should be done *before* showing the solution.
The pieces should be shuffled *after* showing the solution and
*before* producing the puzzle.
