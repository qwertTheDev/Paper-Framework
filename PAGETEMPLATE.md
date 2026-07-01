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
