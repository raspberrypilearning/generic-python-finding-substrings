# Finding sub-strings with Python

Imagine you have a string like "Programming with Python is awesome". And you wanted to find out whether it has the word "with" in the string. How could you go about finding out?

*[string]: A sequence of characters

- Python has a very handy operator called `in`. It can be used to find out whether a data structure such as a string or a list contains a particular element.

- If you open up a simple Python shell (either using IDLE or the Terminal), you can test this operator out.

	```python
	>>> 'a' in 'cat'
	True
	```

- It also works for longer strings, so you can try this:

	```python
	>>> 'with' in 'Programming with Python is awesome'
	True
	>>> 'with Python' in 'Programming with Python is awesome'
	True
	```

- Watch out though, it's case sensitive.

	```python
	>>> 'with python' in 'Programming with Python is awesome'
	False
	```

- If you don't care about case, then you can use the `lower` or `upper` string method to convert the string to a single case.

	```python
	>>> 'with python' in 'Programming with Python is awesome'.lower()
	True
	```

- Another problem you might encounter is looking for only whole words. For instance:

	```python
	>>> 'on' in 'Programming with Python is awesome'.lower()
	True
	```

- As you can see, it found the sub-string `on`, as it's the last two characters in the string `Python`. If you're only looking for single words, then you can split the string up first. This turns it into a list.

	```python
	>>> 'Programming with Python is awesome'.lower().split()
	['programming', 'with', 'python', 'is', 'awesome']
	>>> 'on' in 'Programming with Python is awesome'.lower().split()
	False
	>>> 'python' in 'Programming with Python is awesome'.lower().split()
	True
	```
