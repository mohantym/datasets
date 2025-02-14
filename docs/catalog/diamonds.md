<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="diamonds" />
  <meta itemprop="description" content="This classic dataset contains physical attributes and prices of 53940 diamonds.&#10;&#10;Attributes:&#10;&#10;  * price: Price in US dollars.&#10;  * carat: Weight of the diamond.&#10;  * cut: Cut quality (ordered worst to best).&#10;  * color: Color of the diamond (ordered best to worst).&#10;  * clarity: Clarity of the diamond (ordered worst to best).&#10;  * x: Length in mm.&#10;  * y: Width in mm.&#10;  * z: Depth in mm.&#10;  * depth: Total depth percentage: 100 * z / mean(x, y)&#10;  * table: Width of the top of the diamond relative to the widest point.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;diamonds&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/diamonds" />
  <meta itemprop="sameAs" content="https://ggplot2.tidyverse.org/reference/diamonds.html" />
  <meta itemprop="citation" content="@Book{,&#10;  author = {Hadley Wickham},&#10;  title = {ggplot2: Elegant Graphics for Data Analysis},&#10;  publisher = {Springer-Verlag New York},&#10;  year = {2016},&#10;  isbn = {978-3-319-24277-4},&#10;  url = {https://ggplot2.tidyverse.org},&#10;}" />
</div>

# `diamonds`


*   **Description**:

This classic dataset contains physical attributes and prices of 53940 diamonds.

Attributes:

*   price: Price in US dollars.
*   carat: Weight of the diamond.
*   cut: Cut quality (ordered worst to best).
*   color: Color of the diamond (ordered best to worst).
*   clarity: Clarity of the diamond (ordered worst to best).
*   x: Length in mm.
*   y: Width in mm.
*   z: Depth in mm.
*   depth: Total depth percentage: 100 * z / mean(x, y)
*   table: Width of the top of the diamond relative to the widest point.

*   **Homepage**:
    [https://ggplot2.tidyverse.org/reference/diamonds.html](https://ggplot2.tidyverse.org/reference/diamonds.html)

*   **Source code**:
    [`tfds.structured.diamonds.Diamonds`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/structured/diamonds/diamonds.py)

*   **Versions**:

    *   **`1.0.0`** (default): Initial release.

*   **Download size**: `2.64 MiB`

*   **Dataset size**: `13.01 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Yes

*   **Splits**:

Split     | Examples
:-------- | -------:
`'train'` | 53,940

*   **Features**:

```python
FeaturesDict({
    'features': FeaturesDict({
        'carat': tf.float32,
        'clarity': ClassLabel(shape=(), dtype=tf.int64, num_classes=8),
        'color': ClassLabel(shape=(), dtype=tf.int64, num_classes=7),
        'cut': ClassLabel(shape=(), dtype=tf.int64, num_classes=5),
        'depth': tf.float32,
        'table': tf.float32,
        'x': tf.float32,
        'y': tf.float32,
        'z': tf.float32,
    }),
    'price': tf.float32,
})
```

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('features', 'price')`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script src="https://www.gstatic.com/external_hosted/jquery2.min.js"></script>
<script>
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/diamonds-1.0.0.html";
$(document).ready(() => {
  $("#displaydataframe").click((event) => {
    // Disable the button after clicking (dataframe loaded only once).
    $("#displaydataframe").prop("disabled", true);

    // Pre-fetch and display the content
    $.get(url, (data) => {
      $("#dataframecontent").html(data);
    }).fail(() => {
      $("#dataframecontent").html(
        'Error loading examples. If the error persist, please open '
        + 'a new issue.'
      );
    });
  });
});
</script>

{% endframebox %}

<!-- mdformat on -->

*   **Citation**:

```
@Book{,
  author = {Hadley Wickham},
  title = {ggplot2: Elegant Graphics for Data Analysis},
  publisher = {Springer-Verlag New York},
  year = {2016},
  isbn = {978-3-319-24277-4},
  url = {https://ggplot2.tidyverse.org},
}
```

