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

What kind of error is reported?
> ## Sets are unordered
> As sets are unordered, the order of the elements can be different when you print this.
{: .callout}


> ## Initialising
>
> What does the following program print?
>
> ~~~
> letters = set('Hello world!')
> sorted_letters = list(letters)
> sorted_letters.sort()
> print('Letters in greeting:', sorted_letters)
> ~~~
> {: .python}
{: .challenge}
