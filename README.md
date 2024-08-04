
# Docs Assembler - build documentation like LEGO

## Using interchangeable blocks and fragments of text
 * A strategy that mirrors classes and variables in programming. 
 * It streamlines development.
 * And simplfies editing in growing systems. 

<!-- ![Docs Assembler intro gif](./assets/DocsAssemblerIntro.gif) -->


### Maps
The main building block is a map. 
 * It is a json file - akin to a class in software.

![Docs Assembler json gif](./assets/DocsAssemblerJson.gif)


### Steps
A map holds a section of your documentation, broken down into steps. 
 * Each step points to its own markdown file and holds the documentation text. 
 * Markdown files can be shared between steps. 
 * Markdown files can be edited with the vscode markdown editor.

The Docs Assembler reads these maps and merges the markdown from each step into the output document. 

![Docs Assembler steps gif](./assets/DocsAssemblerSteps.gif)


### Maps can reference other maps
When you refer to a map within another map it just appears as a single step. All the complexity of that map is hidden away from you. If it has exits you can build a chain to other maps or steps. Validation prevents circular references.

![Docs Assembler charts gif](./assets/DocsAssemblerCharts.gif)


**Encapsulation** - wrapping a segment of the documentation within a single map. 
**Inheritance** - where a new map is derived from an existing map (parent).
**Polymorphism** - grouping maps as members of a common superclass of map (tiger, lion => cats).
**Abstraction** - hiding complex documentation details within a map, and exposing that map for reference in others as a single step.
**Composition** - where a map is composed of one or more other maps. 


### Variables
Variables define a piece of markdown text for reuse within other markdown text. 

![Docs Assembler variables gif](./assets/DocsAssemblerVariables.gif)


#### Variables can reference other variables
A variable's markdown text can reference other variables. Validation prevents circular references.

![Docs Assembler variables nested gif](./assets/DocsAssemblerNestedVariables.gif)


### Compiling
On publish the Docs Assembler will read the selected maps, assemble all their referenced maps, markdown files, and expand all the variables, validate it all and assemble it into markdown or HTML files in your repo, or as individuals steps in a database like our system we are ported it from.

![Docs Assembler compiler gif](./assets/DocsAssemblerCompiler.gif)


### Built for complexity
At their simplest a map has single step with a markdown file. Or a single pathway of steps, like a book or a manual. At its most complicated it is a decision tree of scores of steps, many pointing to other maps, which in turn point to other maps. The expanded result could be enormous and impossible to build without being able to break it down into manageable, discrete, reusable, sections, just like we do in code with classes.

![Docs Assembler compiler gif](./assets/DocsAssemblerNetoftrees.gif)


##### Feedback:

This is an experimental port from a c# server/database application to a GitHub repo/extension based on json and markdown files.
This last release focused on markdown and variable files. 
The upcoming release includes options, ancillaries and referencing of maps.
The concept was driven by transformational conversations with a robotics firm, about the difficulties they face with documentation and the solutions they hope for.

If you have any questions or feedback that could help this project email us at team@netoftrees.com 

