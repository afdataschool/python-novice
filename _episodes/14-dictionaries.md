---
title: "Dictionaries"
teaching: 20
exercises: 20
questions:
- "What is a dictionary, and how do I use it?"
objectives:
- "Explain how dictionaries work."
- "Create and access data in a dictionary"
keypoints:
- "A dictionary stores key-value pairs."
- "Dictionaries are unordered."
- "Dictionaries are immutable."
---

## A dictionary groups similar pairs of data together.

* For example, names and research program:

~~~
birthdays = {'Newton': 1642; 'Darwin' 1809}

~~~
{: .python}

Here, 'Newton' and 'Darwin' are keys, and the dates are values.

We can get the value associated with a key by putting the key in square brackets.
* This is like subscripting a string
* Not restricted to integers

~~~
birthdays['Newton']
~~~
{: .python}

New pairs can be added by assigning a value to a key:

~~~
birthdays['Turing'] = 1612
~~~
{: .python}

Turing's birthdate above is actual incorrect. Values may be overwritten by re-assignment:

~~~
birthdays['Turing'] = 1912
~~~
{: .python}

What about if there is nothing assigned to a key?

~~~
birthdays['Nightingale']
'Nightingale' in birthdays
'Darwin' in birthdays
~~~
{: .python}


## For loops and dictionaries

~~~
for name in birthdays:
    print name
~~~
{: .python}

> ## Molecules
> You need to keep track of molecules in the lab, and want to be
> able to look up molecular formulas given a molecule's name. 
>
> silver nitrate: Ag.N.O<sub>3</sub>
>
> chlorine : Cl<sub>2</sub>
>
> sodium chloride :Na.Cl
>
>1. Use a dictionary to represent how many atoms of each element combine to make silver nitrate.
>2. Use a nested dictionary to represent the chemical formula of any of these elements.
>3. How would you look up the number of ions of Cl that combine in sodium chloride?
>4. HARDER: use an accumulator and a for loop to tally the total number of each element in your dictionary?
{: .challenge}

