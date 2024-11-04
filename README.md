# Card-Games
Exercise Learning Goals
This learning exercise helped evolve your knowledge of Lists.

You've unlocked 7 concepts:

Di
Dicts
Li
List Methods
Lo
Loops
Se
Sets
Cl
Classes
Ge
Generators
Un
Unpacking And Multiple Assignment
You've unlocked 97 exercises:

Icon for exercise called Inventory Management
Inventory Management
Icon for exercise called Chaitana's Colossal Coaster
Chaitana's Colossal Coaster
Icon for exercise called Making the Grade
Making the Grade
Icon for exercise called Cater Waiter
Cater Waiter
Icon for exercise called High Scores
High Scores
Icon for exercise called Matrix
Matrix
Icon for exercise called Hamming
Hamming
Icon for exercise called Twelve Days
Twelve Days
Icon for exercise called Scrabble Score
Scrabble Score
Icon for exercise called Grade School
Grade School
Icon for exercise called Luhn
Luhn
Icon for exercise called Tournament
Tournament
Icon for exercise called Book Store
Book Store
Icon for exercise called Robot Name
Robot Name
Icon for exercise called Protein Translation
Protein Translation
Icon for exercise called Phone Number
Phone Number
Icon for exercise called Series
Series
Icon for exercise called Anagram
Anagram
Icon for exercise called Palindrome Products
Palindrome Products
Icon for exercise called Saddle Points
Saddle Points
Icon for exercise called Prime Factors
Prime Factors
Icon for exercise called Matching Brackets
Matching Brackets
Icon for exercise called Pythagorean Triplet
Pythagorean Triplet
Icon for exercise called Sum of Multiples
Sum of Multiples
Icon for exercise called Meetup
Meetup
Icon for exercise called Sieve
Sieve
Icon for exercise called Tree Building
Tree Building
Icon for exercise called Go Counting
Go Counting
Icon for exercise called React
React
Icon for exercise called Secret Handshake
Secret Handshake
Icon for exercise called Largest Series Product
Largest Series Product
Icon for exercise called Connect
Connect
Icon for exercise called Minesweeper
Minesweeper
Icon for exercise called OCR Numbers
OCR Numbers
Icon for exercise called Poker
Poker
Icon for exercise called Rectangles
Rectangles
Icon for exercise called Say
Say
Icon for exercise called Scale Generator
Scale Generator
Icon for exercise called Atbash Cipher
Atbash Cipher
Icon for exercise called Flatten Array
Flatten Array
Icon for exercise called Binary Search Tree
Binary Search Tree
Icon for exercise called Affine Cipher
Affine Cipher
Icon for exercise called Binary Search
Binary Search
Icon for exercise called Variable Length Quantity
Variable Length Quantity
Icon for exercise called Two Bucket
Two Bucket
Icon for exercise called Crypto Square
Crypto Square
Icon for exercise called House
House
Icon for exercise called List Ops
List Ops
Icon for exercise called Robot Simulator
Robot Simulator
Icon for exercise called Roman Numerals
Roman Numerals
Icon for exercise called Linked List
Linked List
Icon for exercise called Change
Change
Icon for exercise called DOT DSL
DOT DSL
Icon for exercise called Knapsack
Knapsack
Icon for exercise called Circular Buffer
Circular Buffer
Icon for exercise called Run-Length Encoding
Run-Length Encoding
Icon for exercise called Transpose
Transpose
Icon for exercise called Grep
Grep
Icon for exercise called Bowling
Bowling
Icon for exercise called Forth
Forth
Icon for exercise called Ledger
Ledger
Icon for exercise called Word Search
Word Search
Icon for exercise called Satellite
Satellite
Icon for exercise called Zipper
Zipper
Icon for exercise called POV
POV
Icon for exercise called Diamond
Diamond
Icon for exercise called Spiral Matrix
Spiral Matrix
Icon for exercise called Food Chain
Food Chain
Icon for exercise called Dominoes
Dominoes
Icon for exercise called REST API
REST API
Icon for exercise called Nth Prime
Nth Prime
Icon for exercise called Rail Fence Cipher
Rail Fence Cipher
Icon for exercise called Zebra Puzzle
Zebra Puzzle
Icon for exercise called Custom Set
Custom Set
Icon for exercise called PaaS I/O
PaaS I/O
Icon for exercise called Alphametics
Alphametics
Icon for exercise called D&D Character
D&D Character
Icon for exercise called Resistor Color
Resistor Color
Icon for exercise called Resistor Color Duo
Resistor Color Duo
Icon for exercise called Space Age
Space Age
Icon for exercise called Hangman
Hangman
Icon for exercise called Rational Numbers
Rational Numbers
Icon for exercise called SGF Parsing
SGF Parsing
Icon for exercise called Simple Cipher
Simple Cipher
Icon for exercise called Ellen's Alien Game
Ellen's Alien Game
Icon for exercise called Plane Tickets
Plane Tickets
Icon for exercise called Wordy
Wordy
Icon for exercise called Markdown
Markdown
Icon for exercise called Locomotive Engineer
Locomotive Engineer
Icon for exercise called Resistor Color Trio
Resistor Color Trio
Icon for exercise called Bottle Song
Bottle Song
Icon for exercise called Killer Sudoku Helper
Killer Sudoku Helper
Icon for exercise called Pascal's Triangle
Pascal's Triangle
Icon for exercise called Resistor Color Expert
Resistor Color Expert
Icon for exercise called Sublist
Sublist
Icon for exercise called All Your Base
All Your Base
Icon for exercise called Eliud's Eggs
Eliud's Eggs
Introduction
A list is a mutable collection of items in sequence. Like most collections (see the built-ins tuple, dict and set), lists can hold reference to any (or multiple) data type(s) - including other lists. Like any sequence, items can be accessed via 0-based index number from the left and -1-based index from the right. Lists can be copied in whole or in part via slice notation or <list>.copy().

Lists support both common and mutable sequence operations such as min()/max(), <list>.index(), <list>.append() and <list>.reverse(). List elements can be iterated over using the for item in <list> construct. for index, item in enumerate(<list>) can be used when both the element index and the element value are needed.

Under the hood, lists are implemented as dynamic arrays -- similar to Java's ArrayList type, and are most often used to store groups of similar data (strings, numbers, sets etc.) of unknown length. Lists are an extremely flexible and useful data structure and many built-in methods and operations in Python produce lists as their output.

Construction
A list can be declared as a literal with square [] brackets and commas between elements:

>>> no_elements = []

>>> no_elements
[]

>>> one_element = ["Guava"]

>>> one_element
['Guava']

>>> elements_separated_with_commas = ["Parrot", "Bird", 334782]

>>> elements_separated_with_commas
['Parrot', 'Bird', 334782]
For readability, line breaks can be used when there are many elements or nested data structures within a list:

>>> lots_of_entries = [
      "Rose",
      "Sunflower",
      "Poppy",
      "Pansy",
      "Tulip",
      "Fuchsia",
      "Cyclamen",
      "Lavender"
   ]
   
>>> lots_of_entries
['Rose', 'Sunflower', 'Poppy', 'Pansy', 'Tulip', 'Fuchsia', 'Cyclamen', 'Lavender']

# Each data structure is on its own line to help clarify what they are.
>>> nested_data_structures = [
      {"fish": "gold", "monkey": "brown", "parrot": "grey"},
      ("fish", "mammal", "bird"),
      ['water', 'jungle', 'sky']
   ]
   
>>> nested_data_structures
[{'fish': 'gold', 'monkey': 'brown', 'parrot': 'grey'}, ('fish', 'mammal', 'bird'), ['water', 'jungle', 'sky']]
The list() constructor can be used empty or with an iterable as an argument. Elements in the iterable are cycled through by the constructor and added to the list in order:

>>> no_elements = list()

>>> no_elements
[]

# The tuple is unpacked and each element is added.
>>> multiple_elements_from_tuple = list(("Parrot", "Bird", 334782))

>>> multiple_elements_from_tuple
['Parrot', 'Bird', 334782]

# The set is unpacked and each element is added.
>>> multiple_elements_from_set = list({2, 3, 5, 7, 11})

>>> multiple_elements_from_set
[2, 3, 5, 7, 11]
Results when using a list constructor with a string or a dict may be surprising:

# String elements (Unicode code points) are iterated through and added *individually*.
>>> multiple_elements_string = list("Timbuktu")

>>> multiple_elements_string
['T', 'i', 'm', 'b', 'u', 'k', 't', 'u']

# Unicode separators and positioning code points are also added *individually*.
>>> multiple_code_points_string = list('अभ्यास')

>>> multiple_code_points_string
['अ', 'भ', '्', 'य', 'ा', 'स']

# The iteration default for dictionaries is over the keys, so only key data is inserted into the list.
>>> source_data = {"fish": "gold", "monkey": "brown"}

>>> multiple_elements_dict_1 = list(source_data)
['fish', 'monkey']
Because the list constructor will only take iterables (or nothing) as arguments, objects that are not iterable will throw a type error. Consequently, it is much easier to create a one-item list via the literal method.

# Numbers are not iterable, and so attempting to create a list with a number passed to the constructor fails.
>>> one_element = list(16)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'int' object is not iterable

# Tuples *are* iterable, so passing a one-element tuple to the constructor does work, but it's awkward
>>> one_element_from_iterable = list((16,))

>>> one_element_from_iterable
[16]
Accessing elements
Items inside lists (as well as items in other sequence types str & tuple) can be accessed via 0-based index and bracket notation. Indexes can be from left --> right (starting at zero) or right --> left (starting at -1).

index from left ⟹






0
👇🏾	1
👇🏾	2
👇🏾	3
👇🏾	4
👇🏾	5
👇🏾
P	y	t	h	o	n
👆🏾
-6	👆🏾
-5	👆🏾
-4	👆🏾
-3	👆🏾
-2	👆🏾
-1





⟸ index from right
>>> breakfast_foods = ["Oatmeal", "Fruit Salad", "Eggs", "Toast"]

# Oatmeal is at index 0 or index -4.
>>> breakfast_foods[0]
'Oatmeal'

>>> breakfast_foods[-4]
'Oatmeal'

# Eggs are at index -2 or 2
>>> breakfast_foods[-2]
'Eggs'

>>> breakfast_foods[2]
'Eggs'

# Toast is at -1
>>> breakfast_foods[-1]
'Toast'
A section of the elements inside a list can be accessed via slice notation (<list>[start:stop]). A slice is defined as an element sequence at position index, such that start <= index < stop. Slicing returns a copy of the "sliced" items and does not modify the original list.

A step parameter can also be used [start:stop:step] to "skip over" or filter the list elements (for example, a step of 2 will select every other element in the range):

>>> colors = ["Red", "Purple", "Green", "Yellow", "Orange", "Pink", "Blue", "Grey"]

# If there is no step parameter, the step is assumed to be 1.
>>> middle_colors = colors[2:6]

>>> middle_colors
['Green', 'Yellow', 'Orange', 'Pink']

# If the start or stop parameters are omitted, the slice will
# start at index zero, and will stop at the end of the list.
>>> primary_colors = colors[::3]

>>> primary_colors
['Red', 'Yellow', 'Blue']
Working with lists
The usage of the built-in sum() function on a list will return the sum of all the numbers in the list:

>>> number_list = [1, 2, 3, 4]
>>> sum(number_list)
10
You can also get the length of a list by using the len() function:

>>> long_list = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J"]
>>> len(long_list)
10
Lists can be also combined in various ways:

# Using the plus + operator unpacks each list and creates a new list, but it is not efficient.
>>> new_via_concatenate = ["George", 5] + ["cat", "Tabby"]

>>> new_via_concatenate
['George', 5, 'cat', 'Tabby']

# Likewise, using the multiplication operator * is the equivalent of using + n times.
>>> first_group = ["cat", "dog", "elephant"]
>>> multiplied_group = first_group * 3

>>> multiplied_group
['cat', 'dog', 'elephant', 'cat', 'dog', 'elephant', 'cat', 'dog', 'elephant']
Lists supply an iterator, and can be looped through/over in the same manner as other sequence types.

#  Looping through the list and printing out each element.
>>> colors = ["Orange", "Green", "Grey", "Blue"]

>>> for item in colors:
...     print(item)
...
Orange
Green
Grey
Blue
For a more in-depth explanation, of loops and iterators, complete the loops concept.

Instructions
Elyse is really looking forward to playing some poker (and other card games) during her upcoming trip to Vegas. Being a big fan of "self-tracking" she wants to put together some small functions that will help her with tracking tasks and has asked for your help thinking them through.

1. Tracking Poker Rounds
Elyse is especially fond of poker, and wants to track how many rounds she plays - and which rounds those are. Every round has its own number, and every table shows the round number currently being played. Elyse chooses a table and sits down to play her first round. She plans on playing three rounds.

Implement a function get_rounds(<round_number>) that takes the current round number and returns a single list with that round and the next two that are coming up:

>>> get_rounds(27)
[27, 28, 29]
2. Keeping all Rounds in the Same Place
Elyse played a few rounds at the first table, then took a break and played some more rounds at a second table ... but ended up with a different list for each table! She wants to put the two lists together, so she can track all of the poker rounds in the same place.

Implement a function concatenate_rounds(<rounds_1>, <rounds_2>) that takes two lists and returns a single list consisting of all the rounds in the first list, followed by all the rounds in the second list:

>>> concatenate_rounds([27, 28, 29], [35, 36])
[27, 28, 29, 35, 36]
3. Finding Prior Rounds
Talking about some of the prior Poker rounds, another player remarks how similarly two of them played out. Elyse is not sure if she played those rounds or not.

Implement a function list_contains_round(<rounds>, <round_number>) that takes two arguments, a list of rounds played and a round number. The function will return True if the round is in the list of rounds played, False if not:

>>> list_contains_round([27, 28, 29, 35, 36], 29)
True

>>> list_contains_round([27, 28, 29, 35, 36], 30)
False
4. Averaging Card Values
Elyse wants to try out a new game called Black Joe. It's similar to Black Jack - where your goal is to have the cards in your hand add up to a target value - but in Black Joe the goal is to get the average of the card values to be 7. The average can be found by summing up all the card values and then dividing that sum by the number of cards in the hand.

Implement a function card_average(<hand>) that will return the average value of a hand of Black Joe.

>>> card_average([5, 6, 7])
6.0
5. Alternate Averages
In Black Joe, speed is important. Elyse is going to try and find a faster way of finding the average.

She has thought of two ways of getting an average-like number:

Take the average of the first and last number in the hand.
Using the median (middle card) of the hand.
Implement the function approx_average_is_average(<hand>), given hand, a list containing the values of the cards in your hand.

Return True if either one or both of the, above named, strategies result in a number equal to the actual average.

Note: The length of all hands are odd, to make finding a median easier.

>>> approx_average_is_average([1, 2, 3])
True

>>> approx_average_is_average([2, 3, 4, 8, 8])
True

>>> approx_average_is_average([1, 2, 3, 5, 9])
False
6. More Averaging Techniques
Intrigued by the results of her averaging experiment, Elyse is wondering if taking the average of the cards at the even positions versus the average of the cards at the odd positions would give the same results. Time for another test function!

Implement a function average_even_is_average_odd(<hand>) that returns a Boolean indicating if the average of the cards at even indexes is the same as the average of the cards at odd indexes.

>>> average_even_is_average_odd([1, 2, 3])
True

>>> average_even_is_average_odd([1, 2, 3, 4])
False
7. Bonus Round Rules
Every 11th hand in Black Joe is a bonus hand with a bonus rule: if the last card you draw is a Jack, you double its value.

Implement a function maybe_double_last(<hand>) that takes a hand and checks if the last card is a Jack (11). If the last card is a Jack (11), double its value before returning the hand.

>>> hand = [5, 9, 11]
>>> maybe_double_last(hand)
[5, 9, 22]

>>> hand = [5, 9, 10]
>>> maybe_double_last(hand)
[5, 9, 10]
