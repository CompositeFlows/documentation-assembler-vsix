
# Docs Assembler - build documentation like Lego

- Reuse of interchangeable **blocks** and **fragments** of text
- A [strategy](#notes) that mirrors **classes** and **variables** in programming
- Streamlines development and simplifies editing on growing or complex systems.
  


This is an experimental port from a c# server/database application - to a GitHub repo/extension. A concept driven by transformational conversations with a robotics firm - [HAL Robotics](https://hal-robotics.com), so their documentation could be edited as markdown files, stored in their git repo, and compiled into manuals, Q&A, client and implementation specific guides etc - all based on a policy of ***edit once to update globally.***

Any questions or feedback email us: team@netoftrees.com 
    


### Maps
- The main building block is a **map**.
- It is a **json** file with a **.tsmap** extension.
- Functions similarly to a **class** in software.
- [Maps are built to scale](#built-to-handle-both-complexity-and-scale)

![Docs Assembler json gif](./assets/DocsAssemblerJson.gif)
  
  

### Steps
- A **map** is a section of documentation divided into **steps**.
- Each **step** links to a **markdown file**, with the step's documentation text, or to another **map**.
- A **Markdown file** can be shared by many **steps**.
- **Markdown files** are editable with the **Visual Studio Code** markdown editor.

![Docs Assembler steps gif](./assets/DocsAssemblerSteps.gif)
  
  

### Maps can reference other maps
- A **map** referenced within another **map**, appears as a single **step**.
- If a referenced **map** has **exits**, other **maps** or **steps** chained onto those **exits**.
- **Validation** prevents circular references.

![Docs Assembler charts gif](./assets/DocsAssemblerCharts.gif)
  
  

### Variables
- **Variables** define reusable **markdown text**.
- **Variables** that define relative links are adjusted - the links will always be valid for the published document they are used in.

![Docs Assembler variables gif](./assets/DocsAssemblerVariables.gif)
  
  

### Variables can reference other variables
- A **variable's** markdown text can reference other **variables**.
- **Validation** prevents circular references.

![Docs Assembler variables nested gif](./assets/DocsAssemblerNestedVariables.gif)
  
  

### Compile to docs
On **publish**, the **Docs Assembler** reads the **maps** selected for **publish** - it **validates** and assembles all referenced **maps**, **markdown files**, expands any **variables**, copies over referenced **assets**, and **compiles** the resuls into **markdown** or **html** files to the **publish** folder in your **repo**. 

![Docs Assembler publish gif](./assets/DocsAssemblerPublish.gif)
  
  

### Compare published to live
Use the **compare view** to view changes between published files and the **docs** folder files.

![Docs Assembler compare gif](./assets/DocsAssemblerCompare.gif)
  
  

### Move published to live
If the changes are as expected, click-move the published files to the **docs** folder. If you use **GitHub Pages**,  **docs** would be the root folder.

![Docs Assembler live gif](./assets/DocsAssemblerLive.gif)
  
  

### Built to handle both complexity and scale
- At its simplest, a **map** has a single **step** and **markdown file**.
- A **map** could be one pathway of **steps**, like a book or manual.
- At its most complicated, it is a **decision tree** of **steps**, many pointing to other **maps**, which in turn point to other **maps** etc. The expanded result could be enormous, and impossible to build without breaking it down into manageable, discrete, reusable, units. Just like we do in code with **classes**.
  

##### Database version: example published output of a map with ancillaries:

![netoftrees C# server/database applications gif](./assets/netoftreesCsharp.gif)
  
  


##### Database version: contributing maps to the example published output shown above:

![netoftrees C# server/database applications gif](./assets/netoftreesCsharpMaps.gif)
  

### Upcoming
- Port from database version
    - projects
    - publish for ancillaries and referenced maps
    - search
    - shape
    - spread
- Docker database + SPA viewer
- Example repository
- Help files
- Light theme

  

### Notes

- **Encapsulation**: Wrapping a segment of the documentation within a single map.
- **Inheritance**: Deriving a new map from an existing map (parent).
- **Polymorphism**: Grouping maps as members of a common superclass (e.g., tiger, lion => cats).
- **Abstraction**: Hiding complex documentation details within a map and exposing that map's interface to other maps as a single step.
- **Composition**: Composing a map of one or more other maps.




### Releases
- 0.2.20
    - Map folders
    - Intellisense and TextMate grammars for steps and variables
