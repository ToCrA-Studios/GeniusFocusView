# GeniusFocusView

**Offline software-project understanding for humans and AI.**

[Deutsche Version](README_DE.md)

![GeniusFocusView project map](screenshots/project-map.png)

> I did not originally plan to build a software-analysis tool. I wanted to build a game.

## Why I built this

When I began developing software with AI coding agents, the speed was exciting. I could turn ideas into working features even though software development had not been my original profession.

As my projects grew, however, I repeatedly hit the same wall: an AI could write code, but it regularly lost its understanding of the project as a whole. Context windows filled up. Tokens were spent rediscovering the same files and relationships. Changes sounded convincing but sometimes made the application slower, broke something elsewhere, or solved a different problem from the one I had actually described.

I did not want to accept that serious AI-assisted development had to work this way.

While trying to build a game, I therefore began building the tool I was missing. That tool became **GeniusFocusView (GFV)**.

GFV is my attempt to give both a human and an AI a stable view of a software project: what exists, what belongs together, how the parts are connected, and where attention is actually needed.

## What GFV does

GFV analyzes a selected software project locally and turns it into a navigable model containing:

- physical files and resources;
- detected software objects;
- relations between those objects;
- proposed systems and subsystems;
- interactive project and detail maps;
- an editable Canvas Studio;
- a structured Markdown export for focused AI context.

It is not intended to replace source code or human judgment. Its purpose is to stop humans and AI from starting at zero every time they need to understand a project.

### A look inside

| Project understanding | System exploration |
| --- | --- |
| ![GFV analysis progress](screenshots/analysis.png) | ![GFV system explorer](screenshots/system-explorer.png) |

| Visual Canvas Studio | Markdown export |
| --- | --- |
| ![GFV Visual Canvas Studio](screenshots/canvas-studio.png) | ![GFV Markdown export](screenshots/markdown-export.png) |

## Why it works offline

Software projects may contain private ideas, unfinished products, customer information, credentials, or intellectual property. I therefore wanted the analysis itself to remain on the user's computer.

GFV does not require an online AI service to analyze a project. Project memory, generated maps, and exports are stored locally. This is intended to protect private work and reduce repeated token usage when working with external AI tools.

## The Canvas idea

The maps show what GFV detected. Canvas Studio explores the next step: allowing a person to draw, arrange, and explain the intended systems of a project in a form an AI can understand later.

An AI should not only see thousands of files. It should understand that components belong to one system, that a connection has a purpose, and that a boundary was deliberately designed by a human.

That is the direction I want to explore further.

## How this connects to S2S

GFV is one part of a larger personal journey. My other application, **S2S**, explores how ideas, planning, project knowledge, AI collaboration, and implementation can be brought together instead of being scattered across disconnected chats and tools.

GFV focuses on understanding the software that already exists. S2S focuses on moving an idea forward. Both projects grew from one practical question:

> How can one person use AI to build serious software without giving up control of the project?

## Why I am publishing it now

GFV is not finished. It will not understand every language, framework, architecture, or relation correctly. Large projects can still expose performance limits. Some maps need better grouping, navigation, and explanations.

Testing only my own projects cannot answer the questions that matter:

- Does GFV help you understand your project?
- Which languages and frameworks does it handle well?
- Which objects, relations, systems, or files does it miss?
- Where is its interpretation wrong?
- Which maps are useful, and which are confusing?
- Does the Markdown export improve your work with an AI?
- Is this a tool I should continue developing?

Honest feedback will help decide what GFV becomes next. A report saying “this part does not work” is useful when it explains what was expected and what happened instead.

## An independent first release

GFV is an independent project in active development. I am releasing this community build to test the idea with real projects and real users instead of developing it only around my own assumptions.

The experiences and feedback from this release will determine which problems I work on next and whether GFV is useful enough to continue developing.

## Download

Download the current macOS build from [GitHub Releases](../../releases/latest).

The application is distributed as a compiled binary. The source code is currently private.

### macOS compatibility

- macOS 10.15 or newer;
- Apple Silicon and Intel Macs;
- performance depends heavily on project size, file count, object count, and available memory.

The first public build is not notarized by Apple. If macOS blocks the first launch, right-click the application, choose **Open**, and confirm the dialog.

### Installing and opening the macOS build

1. Download `GeniusFocusView-macOS-1.0.0.zip` from [GitHub Releases](../../releases/latest).
2. Double-click the ZIP file to unpack it.
3. Move `GeniusFokusView.app` to **Applications** if you want to keep it there.
4. For the first launch, Control-click or right-click the app, choose **Open**, and then choose **Open** again.

Because this independent test build is not yet notarized by Apple, some macOS versions may still report that Apple cannot verify the developer or that the app cannot be opened. In that case:

1. Open **Terminal** from Applications → Utilities.
2. Type the following command, including the final space, but do not press Return yet:

   ```text
   xattr -dr com.apple.quarantine 
   ```

3. Drag `GeniusFokusView.app` from Finder into the Terminal window. Its full path will be added automatically.
4. Press Return, close Terminal, and open the app normally.

Only use this workaround for the GFV build downloaded from this official repository. It removes Apple's download quarantine from that one app; it does not install additional software or change the rest of the system.

## Privacy

- Analysis runs locally.
- GFV does not include analytics or telemetry services.
- GFV writes its project memory into the analyzed project so later runs can reuse previous work.

Always keep backups of important projects. Early software can contain defects, and an analysis tool should never be the only place where important data exists.

## Feedback and bug reports

Please use [GitHub Issues](../../issues) for bugs, missing detections, performance reports, and feature ideas. Reports may be written in English or German.

Helpful reports include:

- Mac model and year;
- macOS version;
- installed memory;
- approximate number of project files;
- primary languages and frameworks;
- how long analysis, map loading, or export took;
- what GFV displayed;
- what you expected it to display.

Please do **not** attach confidential source code, credentials, or private project-memory files.

## About me

I did not begin as a traditional software engineer. My professional background started in consumer electronics and retail, later including operational and management responsibility. I came to software because I wanted to discover what one person could build with a Mac, persistence, and modern AI tools.

That outsider perspective shapes GFV. I do not assume an answer is correct because it sounds technical. I test what actually happens, question contradictions, and keep working when a superficial solution is not good enough.

GeniusFocusView is both a product and part of my own learning process. Publishing it is the next test.

— **TocRa Studios**
