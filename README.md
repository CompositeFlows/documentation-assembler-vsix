
# Docs Assembler - build documentation like Lego

- Reuse of interchangeable **blocks** and **fragments** of text.
- A [strategy](#notes) that mirrors **classes** and **variables** in programming.
- Streamlines development and simplifies editing on growing or complex systems.
  


This is an experimental port from a c# server/database application - to a GitHub repo/extension. A concept driven by transformational conversations with a robotics firm - [HAL Robotics](https://hal-robotics.com), so their documentation could be edited as markdown files, stored in their git repo, and compiled into manuals, Q&A, client and implementation specific guides etc - all based on a policy of ***edit once to update globally.***



### Questions or feedback?
[team@netoftrees.com](mailto:team@netoftrees.com)
    


### Maps
- The main building block is a **map**.
- It is a **json** file with a **.tsmap** extension.
- Functions similarly to a **class** in software.
- [Maps are built to scale](#built-to-handle-both-complexity-and-scale)

![Docs Assembler json gif](./assets/DocsAssemblerJson.gif)
  
  

### Steps
- A **map** is a section of documentation divided into **steps**.
- Each **step** links to a **markdown file** with the step's documentation text.
- **Markdown file** can be shared between multiple **steps**.
- **Markdown files** are editable with the **Visual Studio Code** markdown editor.

![Docs Assembler steps gif](./assets/DocsAssemblerSteps.gif)
  
  

### Maps can reference other maps
- A **map** referenced within another **map**, appears as a single **step**.
- If a referenced **map** has **exits**, other **maps** or **steps** will need chained onto those **exits**.
- **Validation** prevents circular references.

![Docs Assembler charts gif](./assets/DocsAssemblerCharts.gif)
  
  

### Variables
- **Variables** define reusable **markdown text**.
- **Variables** that define relative links are adjusted to be always be valid for the published document they are used in.

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
- A slightly more complex **map** would be a single pathway of **steps**, like a book or manual.
- At its most complicated, a **map** is a **decision tree** of **steps**, many pointing to other **maps**, which in turn point to other **maps** etc. The expanded result could be enormous, and impossible to buildor maintain without breaking it down into manageable, discrete, reusable, units. Just like we do in code with **classes**.
  

## Example of published output


![netoftrees C# server/database applications gif](./assets/netoftreesCsharp.gif)


#### Image above
- This shows the c# server/database application, where **steps** are stored in a database.
    - It has all the **ancillaries** expanded. 
    - When all **ancillaries** are collapsed the **guide** shows enough information for an expert to complete the task. 
    - If a user expands an **ancillary**, they insert more **steps** on a topic. 
    - **Ancillaries** can be nested - so users can drill down.
    - With all possible **ancillaries** expanded, all the **steps** for completing a task, as a novice, are laid out.
- Reusing **maps** makes it straight forward to build and maintain **guides** that a user can tailor to their skill set.

  


#### Image below
- This shows the editor for the c# server/database application.
    - With the referenced maps, including nested ones, used to build the guide shown above.
    - Most will be reused in other guides.

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

- ***Encapsulation*** - Wrapping a segment of the documentation within a single **map**.
- ***Inheritance*** - Deriving a new **map** from an existing **map** (parent).
- ***Polymorphism*** - Grouping **maps** as members of a common superclass (e.g., tiger, lion => cats).
- ***Abstraction*** - Hiding complex documentation details within a **map** and exposing that **map's interface** to other **maps** as a single **step**.
- ***Composition*** - Composing a **map** of one or more other **maps**.




### Releases
- 0.2.34
    - Map folders
    - Intellisense and TextMate grammars for steps and variables
    - Publish listed maps



### Links

[team@netoftrees.com](mailto:team@netoftrees.com)

[www.netoftrees.com](https://www.netoftrees.com/)

[x.com/docsassembler](https://x.com/docsassembler)
