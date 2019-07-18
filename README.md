
# Teacher Notes

## Introduction

This is an introductory exercise to give students additional practice in working with basic python data structures and methods. Encourage students to problem solve by using search engines and accessing documentation. Redemonstrate how to use tab completion to preview the available methods for a variable as well as how to pull up the documentation in jupyter notebook by appending a question mark at the end of a method. For example, once students have instantiated the variable cats, the can append a dot and press tab to see the available methods. From there, they can choose a specific one (such as sort) and pull up the documentation with `cats.sort?`. Giving students soft skills so they can begin building their own programming and problem solving skills independently is critical.

## Learning Goals

* Increase student fluency of lists and string methods
    * Use the append method for strings
    * Use the sort method for lists
    * Iterate over lists using for loops or list comprehensions
* Use a search enginge to problem solve
* Read documentation

## Prerequisite Knowledge

Students should already have some exposure to basic python datatypes. 

## Paired Programming

```cats = [‘Maine Coon’, ‘Tabby’, ’Siamese’, ‘Garfield’, ‘Sylvester’]```

1. Create a new list cat_jrs by appending ‘Jr.’ to each of the cats names.
2. Sort the list in alphabetical order.
3. Look up a new string or list method and explain how it works.

**Bonus:**
    Sort the list by the 3rd letter of each name.


```python
cats = ['Maine Coon', 'Tabby', 'Siamese', 'Garfield', 'Sylvester']
```

# Teacher Notes


Circulate to check student's progress on working with git. If a substantial portion of the class is struggling, bring the group together and ask a volunteer to help lead the class through this process. Assist this volunteer as needed until all students are able to complete the git portion. Then provide an additional 5-10 minutes for students to work on the list exercise itself.

# Potential Solutions:

```python
cat_jrs = [] #Define the new variable cat_jrs (which is a list!!! hence the brackets)
for cat in cats: #Start our for loop
    cat = cat + " Jr." #take this thing each and add "Jr." store it in a variable called cat
    cat_jrs.append(cat) #cat_jrs which is a list object then we're using a method
cat_jrs.sort() #Question 2; Returns None
cat_jrs.sort(key=lambda x: x[2]) #Bonus; good review of lambda functions
```

> Note: It is also worth reviewing alternative solutions to this problem including how to use list comprehensions.

As a list comprehension:
```cat_jrs = [cat + " Jr." for cat in cats]```

> **Common Misconception**: Point out that the alias for the iterable in a for loop is completely arbitrary. (Python does not know the english grammatical rule that a cat is the singular of cats.)  For example, in the above code snippet `for cat in cats` you could just as easily write `for c in cats` or `for item in cats`. You could even write `for superBadVerboseVariableName123 in cats`. The point is that whatever you alias the iterable as is what you should then reference in the indented code block Which will execute for each iteration of the loop. 
