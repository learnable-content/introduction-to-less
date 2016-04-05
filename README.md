![](Introduction_to_Less/headers/4-7.jpg)

#Lesson Files
You can find the lesson files for this lesson [here](https://github.com/learnable-content/introduction-to-less/tree/lesson1.1/intro%20to%20less%20-%20code%20samples/lesson3.7)


# Code Refactoring

In this step we will refactor and clean up our code.

With Less you can keep the code DRY by writing less code and by not repeating yourself. However in the `bottom` section we're using multiple times the class `inline` with the namespace `inline_list`. That's too much, and this is against the principle of writing less code.

First of all, remove all styling for the `inline` class from the `bottom`. Next define the following rule:

```less
#bottom {
 	div {
 	 	.inline {
 	  		#inline_list;
 	 	}
 	}
}
```

This way we are reducing the amount of code duplication.

Now the `h3`:

```less
#bottom {
 	h3 {
		padding-bottom: @padding;
	 	.bordered(xxx, xxx, @light, xxx);
	}
}
```

So now we have polished the design and also refactored and cleaned up the code.
