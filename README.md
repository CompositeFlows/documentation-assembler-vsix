# Docs Assembler - Treat Your Documentation Like Code

***Solve documentation hell,***

- **Sprawling, duplicated content** across guides, manuals, and wikis.
- **Bug-prone updates** Make an edit in one place, miss it in ten others.
- **Brittle, unmanageable docs** that can't handle complex, branching scenarios without becoming a nightmare.
- **Wasting time** wrestling with static generators instead of building features.

***by applying the principles of software engineering to your documentation,***

Docs Assembler is a VS Code extension that lets you build documentation systems with **modular, reusable components**. Think of it like **React for tech docs** or **class-based inheritance for your content**.

- **Maps (.tsmap files)**: Self-contained documentation modules that can be nested and composed, just like classes. Encapsulate procedures, tutorials, or decision trees.
- **Variables**: Define reusable text snippets (e.g., product names, error messages, URLs). Change one, update everywhere.
- **Inheritance & Composition**: Build complex guides from simple, reusable blocks. A change in a base **map** propagates to all guides that use it.
- **Compile to Docs**: Assemble these components on-the-fly into flawless, context-aware Markdown or HTML for your static site (like GitHub Pages).

***and maintain a single source of truth for your documentation.***


## Build documentation like Lego

This is an experimental port from a c# server/database application - to a GitHub repo/vscode extension. A concept driven by transformational conversations with a robotics firm - [HAL Robotics](https://hal-robotics.com), so their documentation could be edited as markdown files, stored in their GitHub Pages repo, and compiled into manuals, diagnostic/solution walkthroughs, manufacturer specific guides etc - all based on a policy of ***edit once - update globally*** - like with **classes** and **components** in code.



### GitHub Pages 
[Modular Documentation Demos](https://muddyturnip.github.io):  
Publish currently targets GitHub Pages, producing Jekyll Markdown.  
After a Publish run a Git Commit and Push for GitHub Pages to make changes live.  

[Repo](https://github.com/MuddyTurnip/MuddyTurnip.github.io):  
The sample maps are located in the `/tsmaps/` folder and published guides in `/docs/`.  

Hosting a website on [GitHub Pages](https://docs.github.com/en/get-started/learning-about-github/githubs-plans) is free for public repos. 



### Bugs, questions or feedback? - Email us
[team@netoftrees.com](mailto:team@netoftrees.com)



### After an extension update clear vscode history:  
- Open the Command Palette: _Cmd+Shift+P_  
- Type: _Clear Editor History_



## Quick walkthrough
Using a fork of the HAL Robotics documentation repo, initialised to use maps - [HAL.Documentation.maps](https://github.com/CompositeFlows/HAL.Documentation.maps).   
It serves as a good example for simple use cases - as there are only shared variables and steps, no linked maps. 
#### BE AWARE: This is not the current version of HAL Robotics documentation - [see below](#for-up-to-date-information-on-hal-robotics)

[<img src="./assets/Walkthrough-thumbnail.png">](https://vimeo.com/1013352380?share=copy#t=0)
    


### Maps
- The main building block is a **map**.
- It is a **json** file with a **.tsmap** extension.
- Functions similarly to a **class** in software.
- [Maps are built to scale up easily](#built-to-handle-both-complexity-and-scale)


#### Switching between **Map Editor** and **Map Json Editor**:

![Docs Assembler map json editor gif](./assets/DocsAssemblerJsonDec24.gif)



#### Switching between **Maps Diff** and **Maps Json Diff**:

![Docs Assembler diff map json gif](./assets/DocsAssemblerDiff.gif)
  
  

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
  


### Released
- 0.6.104
    - Map folders
    - Intellisense, diagnostics and TextMate grammars for steps and variables
    - Publish listed maps
    - Moving or copying map folder corrects relative urls
    - Map json editor
    - Diff map json editor
    - Maps explorer
    - Map hyper links
    - GitHub Pages integration
    - Publish for referenced and nested maps
    - Publish for ancillaries



### Next
- Update GitHub Pages site with a new demo showing referenced and nested map example using ancillaries


### Upcoming
- Video tutorial how to set up and publish to GitHub Pages
- Tutorials and help files
- Port from database version
    - projects
    - search
    - shape
    - spread
- Light theme
- Docker database + SPA viewer

  

### Notes

- ***Encapsulation*** - Wrapping a segment of the documentation within a single **map**.
- ***Inheritance*** - Deriving a new **map** from an existing **map** (parent).
- ***Polymorphism*** - Grouping **maps** as members of a common superclass (e.g., tiger, lion => cats).
- ***Abstraction*** - Hiding complex documentation details within a **map** and exposing that **map's interface** to other **maps** as a single **step**.
- ***Composition*** - Composing a **map** of one or more other **maps**.




### Links

[team@netoftrees.com](mailto:team@netoftrees.com)  
[www.netoftrees.com](https://www.netoftrees.com/)  
[x.com/docsassembler](https://x.com/docsassembler)  


### For up to date information on HAL Robotics:

documentation:
[docs.hal-robotics.com](https://docs.hal-robotics.com/)  
documentation repo:
[github.com/HALRobotics/HAL.Documentation](https://github.com/HALRobotics/HAL.Documentation)  
website:
[hal-robotics.com](https://hal-robotics.com/)  

