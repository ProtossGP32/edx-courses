# Part 3: Matplotlib and Pyplot

## 2.3.1: Introduction to Matplotlib and Pyplot

Video here: [\[LINK\]](media/2.3.1-introduction-to-matplotlib-and-pyplot.mp4)

Check the notebook example [2.3.1-introduction-to-matplotlib-and-pyplot](scripts/2.3.1-introduction-to-matplotlib-and-pyplot.ipynb)

### GOALS:

- Learn how to create simple plots using `matplotlib.pyplot`

### What is Matplotlib?

Matplotlib is a Python plotting library that produces **publication-quality figures**.

### What is Pyplot?

Pyplot is a collection of functions that make Matplotlib work like Matlab.

- Pyplot provides what is sometimes called a state machine interface to Matplotlib library
- `matplotlib.pyplot` is commonly imported as `plt` by virtually everyone who uses this library

> [!NOTE] Installing Matplotlib
> If you're using a conda environment, launch the following command:
> ```bash
> conda install matplotlib
> ```
> Else, use `pip`:
> ```
> pip install matplotlib
> ```
> Make sure you include `matplotlib` in your project's `requirements.txt` file, `pyproject.toml` dependencies or your conda's environment config file afterwards

#### Displaying plots

When working in notebooks, the plots will be shown under each cell. But when working in a Python shell, we need to explicitly tell Python to show the plot in a Desktop window with `plt.show()` just after composing the plot

- The built-in `plt.show()` function takes the currently composed plot in memory and renders it

#### Multiple arguments in Pyplot

You can define the X and Y coordinates of a list of points as separate vectors and pass them as argumetns to the `plt.plot()` function.

> [!NOTE] Introduction to keyword arguments
> Keyword arguments are arguments which are supplied to the function by explicitly naming each parameter and specifying its value.
> 
> Keyword arguments are commonly used in Pyplot to define and adjust the characteristics of the plots.

### Comprehension Check

Please check the lesson's notepad for any question not explained here

#### Question 1

What does `plt.show()` do?

- Show a plot that is already created

#### Question 2

What does `plt.plot([0,1,2],[0,1,4],"rd-")` do?

- A plot of two connected lines, with red diamonds at the junctures

## 2.3.2: Customizing your Plots

Video here: [\[LINK\]](media/2.3.2-customizing-your-plots.mp4)

Check the notebook example [2.3.2-customizing-your-plots](scripts/2.3.2-customizing-your-plots.ipynb)

### GOALS:

- Learn how to customize your plots by adding a **legend** and by **adjusting** and **labeling** the axes
- Learn how to **save** your figures

### Important elements in plots

- `plt.legend()` adds a legend to the plot
- `plt.axis()` adjusts the axis of the plot
- `plt.xlabel()` and `plt.ylabel()` set the axis labels
- `plt.savefig()` saves the current plot figure into a file

> [!NOTE] LaTeX for values
> Pyplot uses LaTeX for composing the plot's text values, so you can take advantage of this.

### Comprehension Check

Please refer to the lesson's notebook for any question not explained here