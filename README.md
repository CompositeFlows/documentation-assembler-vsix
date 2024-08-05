
# Docs Assembler - build documentation like *Lego*

## Using interchangeable *blocks* and *fragments* of text
 * A strategy that mirrors **classes** and **variables** in programming. 
 * It streamlines development.
 * And simplifies editing in growing systems. 

<!-- ![Docs Assembler intro gif](./assets/DocsAssemblerIntro.gif) -->


### Maps
 * The main *building-block* is a **map**. 
 * It is just a **json** file with a **.tsmap** extension.
 * And it is akin to a **class** in software.

![Docs Assembler json gif](./assets/DocsAssemblerJson.gif)


### Steps
 * A **map** holds a section of documentation broken down into **steps**. 
 * Each **step** points to its own **markdown file**, which holds the **step's** documentation text. 
 * **Markdown files** can be shared between **steps**. 
 * **Markdown files** can be edited with the vscode built-in markdown editor.
 * The Docs Assembler reads these **maps** and merges the **markdown** from each **step** into the output document. 

![Docs Assembler steps gif](./assets/DocsAssemblerSteps.gif)


### Maps can reference other maps
 * When you refer to a **map** within another **map** it just appears as a single **step**. 
 * All the complexity of that **map** is hidden away. 
 * If it has **exits** you can build a chain to other **maps** or **steps**. 
 * Validation prevents circular references.

![Docs Assembler charts gif](./assets/DocsAssemblerCharts.gif)


### Variables
 * **Variables** define a piece of **markdown text** for reuse within other **markdown text**. 
 * It could be a link, a table or page of text.
 * **Variables** that are relative links are validated and adjusted to the top-level parent map's directory.

![Docs Assembler variables gif](./assets/DocsAssemblerVariables.gif)


### Variables can reference other variables
 * A **variable's** markdown text can reference other **variables**. 
 * Validation prevents circular references.

![Docs Assembler variables nested gif](./assets/DocsAssemblerNestedVariables.gif)


### Compiling to docs
On publish the Docs Assembler will read the selected maps, recursively assemble all their referenced maps, markdown files, and recursively expand all the variables; validate it all, and compile it into markdown or HTML files into the publish folder in your repo. 

![Docs Assembler publish gif](./assets/DocsAssemblerPublish.gif)


### Comparing published to live
You can then compare the published files with the existing ones using the comparer.

![Docs Assembler compare gif](./assets/DocsAssemblerCompare.gif)


### Replacing live with published
 And if satisfactory click-move the published files to the docs folder which could be configured for GitHub Pages.

![Docs Assembler live gif](./assets/DocsAssemblerLive.gif)


### Compiling to a database
Upcoming releases will include a light theme, publishing support for options, ancillaries, referenced of maps, to Docker database + SPA viewer.

![Docs Assembler compare gif](./assets/DocsAssemblerNetoftrees.gif)


### Built to handle complexity and to scale
 * At its simplest a map has single step with a markdown file. 
 * Or a map could be a single pathway of steps, which is a book or a manual. 
 * At its most complicated, though, it is a decision tree of steps, many pointing to other maps, which in turn point to other maps etc. The expanded result could be enormous and impossible to build without being able to break it down into manageable, discrete, reusable, sections. Just like we do in code with classes.


### Feedback:
This is an experimental port from a c# server/database application to a GitHub repo/extension based on json and markdown files.
The concept was driven by transformational conversations with a robotics firm.

If you have any questions or feedback email us at team@netoftrees.com 


## Object oriented maps:

**Encapsulation** - wrapping a segment of the documentation within a single map. 

**Inheritance** - where a new map is derived from an existing map (parent).

**Polymorphism** - grouping maps as members of a common superclass of map (tiger, lion => cats).

**Abstraction** - hiding complex documentation details within a map, and exposing that map's interface to other maps as a single step.

**Composition** - where a map is composed of one or more other maps. 


