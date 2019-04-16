<div class="cell markdown">

# Here's a demo notebook

This is a demo notebook to play around with the pandoc ipynb support

## Markdown

As it is markdown, you can embed images, HTML, etc into your posts\!

![](outputs/images/ca17e56d65946db885db7f8f50a9605a6a94e6a7.jpg)

Here's one \(inline_{math}\) and

\[
math^{blocks}
\]

<img src="https://upload.wikimedia.org/wikipedia/commons/5/54/Do_i_look_funny_or_something.jpg" />

</div>

<div class="cell markdown" data-tags="[&quot;heresatag&quot;]">

## Cell with metadata

The below cell has some metadata attached to it, let's see how this
looks

</div>

<div class="cell code" data-execution_count="1" data-slideshow="{&quot;slide_type&quot;:&quot;subslide&quot;}" data-tags="[&quot;mytag&quot;,&quot;parameters&quot;]">

``` python
print(2 + 2)
```

<div class="output stream stdout">

``` 
4
```

</div>

</div>

<div class="cell markdown">

## Output types

Here we'll look at a few visualizations

### Matplotlib

</div>

<div class="cell code" data-execution_count="1">

``` python
from matplotlib import rcParams, cycler
import matplotlib.pyplot as plt
import numpy as np
plt.ion()
```

</div>

<div class="cell code" data-execution_count="2">

``` python
# Fixing random state for reproducibility
np.random.seed(19680801)

N = 10
data = [np.logspace(0, 1, 100) + np.random.randn(100) + ii for ii in range(N)]
data = np.array(data).T
cmap = plt.cm.coolwarm
rcParams['axes.prop_cycle'] = cycler(color=cmap(np.linspace(0, 1, N)))


from matplotlib.lines import Line2D
custom_lines = [Line2D([0], [0], color=cmap(0.), lw=4),
                Line2D([0], [0], color=cmap(.5), lw=4),
                Line2D([0], [0], color=cmap(1.), lw=4)]

fig, ax = plt.subplots(figsize=(10, 5))
lines = ax.plot(data)
ax.legend(custom_lines, ['Cold', 'Medium', 'Hot']);
```

<div class="output display_data">

![](outputs/images/a496114900d817d66af2a753c7edf742138585af.png)

</div>

</div>

<div class="cell markdown">

Note that the image above is captured and displayed by Jekyll.

</div>

<div class="cell markdown">

### DataFrames

</div>

<div class="cell code" data-execution_count="5">

``` python
# NO CODE
import pandas as pd
pd.DataFrame([['hi', 'there'], ['this', 'is'], ['a', 'DataFrame']], columns=['Word A', 'Word B'])
```

<div class="output execute_result" data-execution_count="5">

``` 
  Word A     Word B
0     hi      there
1   this         is
2      a  DataFrame
```

</div>

</div>

<div class="cell markdown">

You can configure the text that *Textbooks with Jupyter* uses for this
by modifying your site's `_config.yml` file.

</div>

<div class="cell markdown">

### Folium + Interactive

We can even do the same for *interactive* material. Below we'll display
a map using `ipyleaflet`. When the notebook is converted to Markdown,
the code for creating the interactive map is retained.

**Note that this will only work for some packages.** They need to be
able to output standalone HTML/Javascript, and not depend on an
underlying Python kernel to work.

</div>

<div class="cell code" data-execution_count="1">

``` python
import folium
```

</div>

<div class="cell code" data-execution_count="3">

``` python
m = folium.Map(
    location=[45.372, -121.6972],
    zoom_start=12,
    tiles='Stamen Terrain'
)
m
```

<div class="output execute_result" data-execution_count="3">

    <folium.folium.Map at 0x7ffc988df208>

</div>

</div>

<div class="cell markdown">

## Bibliography

Let's test the bibliography here

Testing this \[bibliography @holdgraf\_rapid\_2016\]

@holdgraf\_evidence\_2014

</div>

<div class="cell markdown">

### The actual bibliography

::: {\#refs} :::

</div>
