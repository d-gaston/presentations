# The Three E's of Learning from Code

Being able to learn from code is one of the most important skills for developers of all levels, since more time is spent reading/interacting with/modifying existing code than writing brand new code. Knowing how to approach and think about an unfamiliar code base systematically will make this process much more productive. These three steps provide a framework where we gather information (**Examine**), form and test hypotheses (**Experiment**), and apply our knowledge (**Extend**).

## Examine
This step is mostly about _reading_ code. Here are some questions that we should ask during this activity.

Here are some questions to keep in mind:
- **Function/Method**
    - Why is it named the way it is? Is it a good name?
        - A good name is a name that conveys the purpose of an entity in the code base.
    - What are the names of the parameters and local variables?
        - What are their types?
        - Where are they used in the function/method?
        - Are they well named? 
    - How does the information flow?
    - What does it return, if anything? What is the type of the return value?
        - (i.e. is it a _pure_ or _impure_ function?)
    - Does it modify any data from a higher scope?
    - What are the control structures (conditionals and loops)? How are they being used? 
    - Does it call other functions/methods?

- **Class**
    - Why is it named the way it is? Is it a good name?
    - What are the names of the methods and attributes?
        - Which methods are modifying which attributes, if any?
        - Ask the function/method questions above about each method
    - Where is this class used elsewhere in the code? 
    - Does this class rely on other classes? (look at import statements)
    - How do you make an instance of this class?

As you answer these questions **LEAVE COMMENTS** documenting what you've learned so your effort doesn't go to waste, since you **WILL** forget important details.
    
## Experiment
Since programs are meant to be run, we will only get so far statically examining code. Experimenting requires us to both be able to _run__ the code _observe_ its behavior.

### Running the code
A program is made up of many pieces of code. Sometimes we'll want to run it all, other times we'll want to isolate a single piece (a class or function) and run it.

1. What inputs does the code require?
    - A number, a list, a dictionary, a text file?
    - Follow up: are there any interesting inputs you could pass?
        - Big numbers, small numbers, empty string, random characters, etc
2. What setup do I need to do?
    - Creating objects, dictionaries, lists, other objects, etc to pass into functions/methods
        - If setup requires several steps, make a script that contains those steps!

    


### Observing the code
If you don't know:
- The type of a variable
- What a function returns
- The possible values a variable can have on a given line

Then you **need** to run the program in such a way that this information is presented to you. This can be done with:
- Logging (i.e. print statements)
    - Snapshot of the value of a variable at a given point
- Debugging
    - When we need an interactive checkpoint in our code which **pauses execution**
    - Useful for: 
        - Complex objects: we don't know what we should/could print out.
        - Expensive operations: our program takes minutes to run and we don't want to have to re-run it multiple times to figure out what information we need.

### Optional: Modifying the code
Sometimes we won't understand why a piece of code is written a certain way. The quickest way to find out is to change it and see what happens! 
- Flip the conditional: < to >, true to false, `and` to `or`, etc
- Change a constant value
- Comment out a block of code



Again, **write down what you've learned!**

## Extend
Extending the program is where we actually do something useful to move us towards whatever goal we had in mind. An extension could be adding code to an existing function/method/class or creating a completely new one. By first examining and experimenting, we will have a better idea of how our extension will fit into and interact with the rest of the code. 

### Before Questions:
- Do you understand the code you're extending _enough_? (Often we do not have the time to learn every single detail)
    - You may think you understood it but then encounter some unexpected behavior. In this case go back to the previous steps
- What are you trying to do? 
    - _write it down in a brief comment_!

### After Questions
- How can you make sure your extension does what you want? (how can you _test_ it?)
- How can you make sure your extension hasn't broken other parts of the code?
    - Make sure your experiments from before do the same thing after you've written your extension.
        - If you saved your earlier experiments in a script, congratulations, you have a _test suite_!
- How can you explain what you've done to others (or to yourself in the future)? 
    - i.e. what _documentation_ do you need to write?

