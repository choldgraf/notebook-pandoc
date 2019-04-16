---
jupyter:
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---

::: {.cell .markdown}
Here\'s a demo notebook
=======================

This is a demo notebook to play around with the pandoc ipynb support.

This is a markdown cell...it should be **rendered as markdown!**

As it is markdown, you can embed images, HTML, etc into your posts!

![](funny.jpg)

:::

::: {.cell .code execution_count="5"}
``` {.python}
# NO CODE
import pandas as pd
pd.DataFrame([['hi', 'there'], ['this', 'is'], ['a', 'DataFrame']], columns=['Word A', 'Word B'])
```
:::

::: {.cell .markdown}
# And this one should also include the output!
:::

::: {.cell .code execution_count="5"}
``` {.python}
# NO CODE
import pandas as pd
pd.DataFrame([['hi', 'there'], ['this', 'is'], ['a', 'DataFrame']], columns=['Word A', 'Word B'])
```

::: {.output .execute_result execution_count="5"}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Word A</th>
      <th>Word B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>hi</td>
      <td>there</td>
    </tr>
    <tr>
      <th>1</th>
      <td>this</td>
      <td>is</td>
    </tr>
    <tr>
      <th>2</th>
      <td>a</td>
      <td>DataFrame</td>
    </tr>
  </tbody>
</table>
</div>
:::
:::