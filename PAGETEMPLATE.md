## Time to create!

Welcome to the **Template Page Document**!
You will now be learning how to structure your pages correctly.

### The basis
**Paper separates the Server and Client environments**
- You can have 2 pages with the same name do different things in different environments.
> Pages must have unique names in the same environment.

**Pages go through Init and Start stages**
- As mentioned in the README, pages will go through this lifecycle.

## Page creation structure
To give a name to your page, you just have to define it inside the Module's table.

    local Page = {
      Name = "Combat"
    }

    or

    local Page = {}
    Page.Name = "Combat"
**Leaving it nameless will have it ignored by Paper.**

Pages can also have a Priority field so your pages **are initialized** in a specific order.

    local Page = {
        Name = "Combat",
        Priority = 2
    }

    local Page = {
        Name = "StateMachine",
        Priority = 1
    }

Pages must have Init() and Start() functions in order to work
but it isn't required **if making a utility module that doesn't run code by itself.**

A reference to Paper will be passed through the Init function, allowing you to use its functions

        function Page:Init(paper)--v
            self.Paper = paper <---<
            self.AnimationHandler = self.Paper:Read("AnimationHandler")
        end
This doesn't occur in the Start function.

## Page example

        local Page = {
            Name = "Console"
        }

        function Page:Init(paper)
            self.Paper = paper
            self.Signal = self.Paper:Read("Signal")
        end

        function Page:Start()
            print("console.log("i don't know javascript")")
            
            self.Signal:Create("onLarped", function()
                warn("Larping detected")
            end)
        end

        return Page

