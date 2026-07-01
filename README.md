
	Welcome to Paper Framework!

	Paper is your personal notebook to make organizing your systems simpler and more intuitive.
	With its page-based structure and simple premise, you can read your systems faster than you can read this documentation.

	Paper's existence isn't to replace any methods you may find better. If anything, this framework takes traditional methods that WORK, and fixes the problems that come with.

--------------------------------------------------------------------------------------

	// Getting Started

	First, require Paper in your script:

	local Paper = require(path.to.Paper)

	Then, register your pages and start the system:

	Paper:AddAuto() -- or use AddPage / AddPages manually
	Paper:Init()
	Paper:Start()
	
	Shared Pages are automatically added, no function needed.
	
	IMPORTANT!!!
	Do NOT run any code that relies on other pages or modifies game features IN THE INIT FUNCTION
	You can only use the Start function for this!!

--------------------------------------------------------------------------------------

	// Core Functions

	* AddPage(page)
  		Manually register a single Page.

	* AddPages(folder)
  		Register multiple Pages from a folder (recursive).

	AddAuto()
  		Automatically registers Pages based on the current environment (Server/Client).

	* Init()
  		Initializes all Pages (sets up dependencies).

	* Start()
  		Starts all Pages (runs logic, connects events).
  		
  	* Write()
  		Writes to Paper's configuration file.
  		It's useful for keeping any data you want to share between your pages.

--------------------------------------------------------------------------------------

	// Environments

	Paper automatically separates Server and Client environments.
	This also occurs in the Explorer.

	* Server Pages only exist on the server
	* Client Pages only exist on the client

	Pages with the same name can exist in both environments with different behavior.
	A Shared folder can be used to share code between them.

--------------------------------------------------------------------------------------

	// Accessing Pages

	Use Paper to access your Pages:

	local Combat = Paper:Read("Combat")

	Avoid requiring Page modules directly.
	Paper exists to manage and connect them.

--------------------------------------------------------------------------------------

	// Writing to Paper
	
	You can write to the Paper file using the Write function:
		ex.: Paper:Write("MaxJumpPower", 80)
		
	That data is stored in the Paper file, and can be accessed by other pages.

--------------------------------------------------------------------------------------

	// Important Rules

	* Pages must have a unique `Name`
	* Pages cannot be added after `Init()` runs
	* Do not modify Pages directly through references
  	    Use functions inside the Page instead

--------------------------------------------------------------------------------------

	// Notes

	A Template Page is included as a reference.
	You can remove it, but it's recommended to keep it for learning.

	This is an early (alpha) version of Paper, so things may change.
	
	I appreciate you considering Paper Framework, and I hope it can help you with your projects.
	Paper Framework isn't supposed to replace any method you may have seen or used before.
	It's designed to fix the problems you may have had, and to be easy to use.

--------------------------------------------------------------------------------------

> Paper Framework Alpha
