## Heya!

Welcome to Paper Framework!

Paper is your personal notebook to make organizing your systems simpler and more intuitive.

Paper doesn't try to reinvent Roblox development. It uses patterns that already work and focuses on making them cleaner, easier to navigate, and more enjoyable to use.

-----------------------------------------------------------------------------

## Time to get started!

Paper Framework uses a **Single Script Architecture**.

That means you only need **one server script** and **one client script** to initialize Paper. From there, your pages are loaded automatically and can communicate with one another.
> Instead of making dozens of LocalScripts in a ScreenGui, let a page handle it!

**"Hold up... pages?"**

Yep!
Around here, ModuleScripts are called **Pages.**

Just like pages in a notebook, each one contains a piece of your game. Together, they make up your notebook.

-----------------------------------------------------------------------------

## How does it work?

Paper manages your structure so you don’t have to wire everything manually.

### The Paper way of things
1. Register pages - Paper discovers all your Modules (Pages).
2. Initialize - dependencies are prepared and linked.
3. Start - your game logic runs.

That’s it. No extra setup steps needed.

**But what if my page loads before another?**

Paper only needs three calls to get everything running:

	Paper:AddAuto() – Registers your default server/client pages
	Paper:Init() – Prepares dependencies between pages
	Paper:Start() – Starts execution
> You can also organize additional folders using Paper:AddPages(folder)

Pages can access each other using Paper:Read("PageName").

If you ever need it, the functions inside Paper's source code come with instructions.
