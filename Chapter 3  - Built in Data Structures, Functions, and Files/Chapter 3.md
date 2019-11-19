# Built-in Data Structures, Functions, and Files

* * *


**Data Structures and Sequences**

* Tuple

    * Sequence of Python Objects

    * Fixed-length

    * Immutable

* List

    * Variable-length 

    * Contents can be modified in-place

**Built-In Sequence Functions**

* Enumerate

    * It’s common when iterating over a sequence to want to keep track of the index of the current item

* Sorted

* Zip

    * Zip can take an arbitrary number of sequences, and the number of elements it produces is determined by the *shortest* sequence.

* Creating dicts from sequences

    * In [1] : mapping = dict(zip(range(5), reversed(ranged(5))))

    * In [2] : mapping

    * Out[2] : {0: 4, 1: 3, 2: 2, 3: 1, 4: 0}

* Default Values

* Valid dict key types

* set	

    * A set is an unordered collection of unique elements. You can think of them like dicts, but keys only, no values.

**List, Set, and Dict Comprehensions**

* *List comprehensions *are one of the most-loved Python language features. They allow you to concisely form a new list by filtering the elements of a collection, transforming the elements passing the filter in one concise expression. 

**Functions**

* Primary and most important method of code organization and reuse in Python

**Namespaces, Scope, and Local Functions**

* Functions can access variables in two different scopes

    * Global and local

* An alternative and more descriptive name describing a variable scope in Python is a *namespace*.

**Returning Multiple Values**

* Python has the ability to return multiple values from a function with simple syntax

    * Example:

		def f():

			a = 5

			b = 6

			c = 7

			return a, b, c

		a, b, c = f()

**Functions are Objects**

* Many constructs can be easily expressed that are difficult to do in other languages

* Suppose we were doing some data cleaning and needed to apply a bunch of transformation to the following list of strings:

In[1] : states = [‘Alabama’, ‘Georgia!’, ‘Georgia’, ‘georgia’, ‘FlOrida’, ‘south carolina###’, ‘West virginia?’ ]

* Anyone who has ever worked with user-submitted survey data has seen messy results like these. Lots of things need to happen to make this list of strings uniform and ready for analysis: stripping whitespace, removing punctuation symbols, and standardizing on proper capitalization.

* One way to do this is to use built-in string methods along with the *re *standard library module for regular expressions:

import re

def clean_strings(strings):

	result = []

	for value in strings:

		value = value.strip()

		value = re.sub(‘[!#?]’, ‘’, value)

		value = value.title()

		result.append(value)

	return result

* The results looks like this:

In  [1] : clean_string(states)

Out [1] : 

[ ‘Alabama’,

‘Georgia’, 

‘Georgia’, 

‘Georgia’, 

‘Florida’,

‘South Carolina’,

‘West Virginia’]

**Anonymous (Lambda Functions)**  

* Python has support for so-called *anonymous *or *lambda *functions

* Are a way of writing functions consisting of a single statement, the result of which is the return value.

* They are defined with the *lambda *keyword, which has no meaning other than "we are declaring an anonymous function":

def short_function(x):

		return x * 2

	Equivalent_anonymous = lambda x : x * 2

**Currying: Partial Argument Application**

* *Currying *is computer science jargon

* It means deriving new functions from existing ones by *partial argument application*

* For example, suppose we had a trivial function that adds two numbers together

def add_numbers(x, y):

	return x + y

* Using this function, we could derive a new function of one variable, *add_five*, that adds 5 to its argument:

add_five = lambda : add_numbers(5, y)

* The second argument to add_numbers is sad to be *curried*.

* There’s nothing very fancy here, as all we’ve really done is define a new function that calls an existing function.

* The built-in *functools* module can simplify this process using the *partial* function:

from functools import partial

add_five = partial(add_number, 5)

**Generators**

* A concise way to construct a new iterable object

* Whereas normal functions execute and return a single result at a time, generators return a sequence of multiple results lazily, pausing after each one until the next one is requested.

* To create a generator, use the *yield* keyword instead of *return *in a function

def squares(n = 10):

	print(‘Generating squares from 1 to {0}’.format(n ** 2))

	for i in range(1, n + 1):

	yield i ** 2

* When you actually call the generator, no code is immediately executed:

In  [1] : gen = sequares()

In  [2] : gen

Out [2] : <generator object squares at 0x7fbbd5ab4570>

* It is not until you request elements from the generator that it begins executing its code:

In [3] : for x in gen:

		print(x, end=’ ’)

Generating squares from 1 to 100

1 4 9 16 25 36 49 64 81 100

**Errors and Exception Handling**

* Handling Python errors or exceptions gracefully is an important part of building robust programs.

**Files and the Operating System**

**Bytes and Unicode with Files**

**Conclusion**

* With some of the basics and the Python environment and language now under our belt, it’s time to move on and learn about NumPy and array-oriented computing in Python

