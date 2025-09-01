Below is the provided intro text for the Docs Assembler demo website, followed by a lead-in to the Lǜ Sēnlín Technologies guide, designed to showcase how Docs Assembler can create a complex, branching product selection guide. The lead-in introduces the fictitious Lǜ Sēnlín Technologies Frame Tower system, highlights its modular and customizable nature, and invites users to explore the guide as a demonstration of Docs Assembler’s capabilities. The tone is professional, engaging, and aligns with the developer-focused philosophy of Docs Assembler, emphasizing modularity and scalability. The content is wrapped in an `<xaiArtifact>` tag with a new `artifact_id` since it’s a distinct section for the demo website’s homepage, per the guidelines.

<xaiArtifact artifact_id="9fdb9365-c74d-468d-8cdd-1ef78b42db2d" artifact_version_id="5500ee80-3857-4529-be30-6d7166badc04" title="Docs_Assembler_Homepage.md" contentType="text/markdown">

# Tame Documentation Hell: Treat Your Docs Like Code

If you’re a developer, you know the pain of "documentation hell." It’s not just about writing docs—it’s about maintaining them. You’re likely all too familiar with the symptoms:

*   **Sprawling, duplicated content** that multiplies across guides, manuals, and wikis, making it impossible to know what’s accurate.
*   **Bug-prone updates:** You make a critical edit in one place, only to miss that same information duplicated in ten other files, instantly introducing inconsistencies.
*   **Brittle, unmanageable docs** that collapse under their own weight when you try to document complex, branching real-world scenarios.
*   **Wasting precious time** wrestling with static site generators and build scripts instead of writing code and building features.

What if you could solve this by applying the proven principles of software engineering directly to your documentation?

That’s the core idea behind **Docs Assembler**, a VS Code extension designed to help you build documentation systems with **modular, reusable components**. Think of it as **React for tech docs** or bringing **class-based inheritance** to your content. It allows you to finally create a system where your documentation is as maintainable and scalable as your codebase.

## Designed for Developers, by Developers

The design of Docs Assembler was driven by a fundamental need from teams like [HAL Robotics](https://hal-robotics.com): to have a powerful system that *respects developer workflows and sovereignty*. This isn't just a tool; it's a philosophy built on core principles that will feel immediately right:

*   **Familiarity & Control:** The entire system is built on the tools you already know and trust. Your documentation lives in **Git repos**, right alongside your code. Content is written in **Markdown files**, editable in any editor. Structure is defined in **JSON files** you can view and edit manually. There’s no new ecosystem to learn.
*   **Absolute Ownership:** You have **physical possession of your documentation**. It's your Markdown and JSON in your repo. You are never locked into a subscription or held ransom by a SaaS platform.
*   **Zero Lock-In:** This is a critical feature. **There are no consequences if you stop using Docs Assembler.** Since it publishes standard Markdown, you can uninstall the extension and your documentation is still perfectly usable, editable, and ready for any other static site generator. Your content is always yours.
*   **Seamless Publishing:** It’s designed to publish directly to **GitHub Pages**, a platform every developer already understands. Even Liquid scripts embedded in your Markdown work as expected.
*   **Built to Scale:** Like classes break down massive software systems, Docs Assembler's modules are designed to decompose enormous documentation sets into manageable, distributable units that different teams can own.
*   **Engineering Rigor:** It brings true software tooling to docs, with **IntelliSense for variables, full validation before publish, and automatic adjustment of relative URLs** when moving files, preventing broken links and ensuring robustness.

## How It Works: The Building Blocks

Docs Assembler introduces key concepts that leverage this philosophy:

*   **Maps (.tsmap files):** These are the core building blocks—self-contained documentation modules (JSON files) that can be nested and composed, just like classes. Each Map can encapsulate anything from a simple procedure to an entire troubleshooting tutorial.
*   **Variables:** Define reusable text snippets for product names, error messages, or URLs. Change the variable in one place, and that change propagates everywhere it’s referenced, eliminating an entire class of errors.
*   **Inheritance & Composition:** Build sophisticated guides from simple, reusable blocks. A change to a base “Map” automatically propagates to all guides that use it.
*   **Compile to Docs:** The system assembles these components on-the-fly into clean, standard Markdown, ready for GitHub Pages. The result? You **maintain a single source of truth for your documentation**, not a dozen fractured copies.

### Build Documentation Like Lego

This entire system was proven in practice with HAL Robotics. They needed a way to manage documentation that could be edited as Markdown in Git, and then compiled into various outputs—user manuals, diagnostic walkthroughs, manufacturer-specific guides—all from a central source.

The driving principle is ***edit once - update globally***. Much like how you use classes and components in code, you define a piece of knowledge once and reuse it everywhere. This transforms documentation from a static, high-maintenance chore into a dynamic, scalable, and truly integrated part of your development workflow.

### Where Are We Trying To Take This?

**This is more than just better documentation. Docs Assembler is a Decision Intelligence Platform. It’s about creating a structured, actionable source of truth for complex operations.**

Consider managing emergencies at an oil refinery. The variables are endless: fires, explosions, earthquakes, power loss, IT failures, medical emergencies. The number of internal teams—incident commanders, operators, maintenance, security, medical, PR, IT, legal, HR—is large, and each needs tailored, timely steps. External stakeholders like emergency services and media introduce more jurisdiction-specific requirements. Add in site variability like equipment locations and local laws, and the complexity is staggering.

**Now imagine capturing all of that in a single, maintainable system.** Each team builds and maintains their own domain-specific maps. The result is a unified, validated, and always up-to-date source of truth that can guide a entire organization through a crisis.

This structured knowledge base is also the perfect foundation for the future. On top of it, you could have a guide front-end (as shown in the HAL example) or a powerful **conversational interface powered by a Graph-Augmented LLM**—an AI that can answer complex questions and generate precise guidance because it’s grounded in your company’s specific knowledge, not just general information.

**This is the destination: turning trapped expertise into a dynamic, accurate, and actionable intelligent asset.**

### See It In Action: This Website Is The Guide

This website is not just talking about Docs Assembler—it is a live demonstration of it. Every page, every word you're reading has been dynamically assembled from a complex structure of interconnected maps.

Under the hood, this entire site is a single guide, built from many modular maps that reference others, creating a scalable hierarchy of knowledge. It demonstrates that you can create and maintain a complex documentation system with a similar ease to how you maintain your codebase.

The very document you are reading was assembled on-the-fly based on the path you've taken through the guide.

To see the mechanics: Look at the section above titled 'Where Are We Trying To Take This?.' It is a single step in the opening map. Click the ancillary button underneath it - 'show the step' to see a screenshot of that exact step open in VS Code and drill into the features behind it. An ancillary is Docs Assembler's way of letting you expand information on-demand, without cluttering the main path for those who don't need it.

This is the proof. This is what treating docs like code looks like.

# Docs Assembler - Treat Documentation Like Code

This is an experimental port from a c# server/database application - to a GitHub repo/vscode extension. A concept driven by transformational conversations with a robotics firm - [HAL Robotics](https://hal-robotics.com).

***Solve documentation hell,***

- **Sprawling, duplicated content** across guides, manuals, and wikis.
- **Bug-prone updates** make an edit in one place, miss it in ten others.
- **Brittle, unmanageable docs** that can't handle complex, branching scenarios without becoming a nightmare.
- **Wasting time** wrestling with static generators instead of building features.

***by applying the principles of software engineering to your documentation,***

Docs Assembler is a VS Code extension that lets you build documentation systems with **modular, reusable components**. Think of it like **classes for your content**.

- **Maps (.tsmap files)**: Self-contained documentation modules that can be nested and composed, just like classes. Encapsulate procedures, tutorials, or decision trees.
- **Variables**: Define reusable text snippets (e.g., product names, error messages, URLs). Change one, update everywhere.
- **Inheritance & Composition**: Build complex guides from simple, reusable blocks. A change in a base **map** propagates to all guides that use it.
- **Compile to Docs**: Assemble these components on-the-fly into flawless, context-aware Markdown or HTML for your static site (like GitHub Pages).

***and maintain a single source of truth for your documentation.***

## Designed for Developers, by Developers

The design of Docs Assembler was driven by a fundamental need to have a powerful system that *respects developer workflows and sovereignty*:

*   **Familiarity & Control:** The entire system is built on the tools you already know and trust. Your documentation lives in **Git repos**, right alongside your code. Content is written in **Markdown files**, editable in any editor. Structure is defined in **JSON files** you can view and edit manually. 
*   **Absolute Ownership:** You have **physical possession of your documentation**. It's your Markdown and JSON in your repo. You are never locked into a subscription or held ransom by a SaaS platform.
*   **Zero Lock-In:** This is a critical feature. **There are no consequences if you stop using Docs Assembler.** Since it publishes as standard Markdown, you can uninstall the extension and your documentation is still perfectly usable, editable, and ready for any other static site generator. Your content is always yours.
*   **Seamless Publishing:** It’s designed to publish directly to **GitHub Pages**, a platform most developers already understand. Even Liquid scripts embedded in your Markdown work as expected.
*   **Built to Scale:** Like classes break down massive software systems, Docs Assembler's modules are designed to decompose enormous documentation sets into manageable, distributable units that different teams can own.
*   **Engineering Rigor:** It brings true software tooling to docs, with **IntelliSense for variables, full validation before publish, and automatic adjustment of relative URLs**.


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
- 0.6.105
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



</xaiArtifact>