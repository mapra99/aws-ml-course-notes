# Software Engineering Practices

## Clean and Modular Code

Code is clean when it is readable, simple and concise. Some tips for this

### Use Meaningful Names

This helps you avoiding the need to explain most of the code with comments.

Bad:

```python
s = [88, 92, 79, 93, 85] # student test scores
print(sum(s)/len(s)) # prints mean of test scores

s1 = [x ** 0.5 * 10 for x in s] # curve scores with square root method and store in new list
print(sum(s1)/len(s1)) # print mean of curved test scores
```

Good:

```python
import math
import numpy as np

test_scores = [88, 92, 79, 93, 85]
print(np.mean(test_scores))

curved_test_scores = [math.sqrt(score) * 10 for score in test_scores]
print(np.mean(curved_test_scores))
```

Guidelines:

- Be descriptive and imply type

  A variable that stores a list can be called with the `_list` suffix, (e,g, `age_list`)

  A boolean variable can start with `is_` or `has_` (e,g, `is_minor`)

- Don't use single-letter variables, except for some well-known letters that are often used with a single purpose, such as `i`, `x`, `y`, `t`, etc.

- Try to avoid the use of abbreviations.

- Use verbs for functions and nouns for variables.

- Be descriptive, but not with more characters than necessary

- Be consistent with white-spacing. indentation, etc.

- Try to limit the lines of a file to around 79 characters.

### Writing Modular Code

Modularity means that the program is logically broken up into clean, reusable modules.

Splitting code into logical modules allows the reusability of existing instances, instead of spending time creating new stuff.

## Refactoring

It's difficult to know how good is code before it is finished. Therefore it is sometimes necessary to go back and refactor existing code.

Advantages:

- Reduce workload in long run (in long-term)
- Easier to maintain code
- Reuse more of your code
- Become a better developer

