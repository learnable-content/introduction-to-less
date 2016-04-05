![](Introduction_to_Less/headers/4-3.jpg)

#Lesson Files
You can find the lesson files for this lesson [here](https://github.com/learnable-content/introduction-to-less/tree/lesson1.1/intro%20to%20less%20-%20code%20samples/lesson3.3)


# Introduction

In this step we're going to continue with the header section and take care of the top section.

# Styling Navigation section

We will use mixins from the *grid.less* file which is the Semantic Grid system.

```less
header {
  background: url("@{bg}skyline_ny.jpg");
  background-size: cover;
  height: 500px;

  #topbar {
  	.bar;
		h2 {
			.column(6);
			padding-top: @padding/2;
			color: darken(@asbestos, 20%);
		}
  	nav {
  		.column(6);
  		float: right;
  		ul {
  			.reset;
  			li {
  				display: inline-block;
  				width: 5rem;
  				margin: @margin;
  				text-align: center;
					a {
						#navigation > .links();
					}
  			}
  		} 			
  	}  	
  	.clearfix();
		}
	}
}
```

`bar` includes a collection of CSS properties that we're going to need to design at the to pbar in the header section.

Using `column` we create the two-column layout. It accepts values between 1 and 12 in order to create the columns. By providing `6` for each elements we get  two columns of an equal width.

The `clearfix` is used to fix problems caused by `float`.

Check the result in your browser!
