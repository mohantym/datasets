<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="cassava" />
  <meta itemprop="description" content="Cassava consists of leaf images for the cassava plant depicting healthy and&#10;four (4) disease conditions; Cassava Mosaic Disease (CMD), Cassava Bacterial&#10;Blight (CBB), Cassava Greem Mite (CGM) and Cassava Brown Streak Disease (CBSD).&#10;Dataset consists of a total of 9430 labelled images.&#10;The 9430 labelled images are split into a training set (5656), a test set(1885)&#10;and a validation set (1889). The number of images per class are unbalanced with&#10;the two disease classes CMD and CBSD having 72% of the images.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;cassava&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;&lt;img src=&quot;https://storage.googleapis.com/tfds-data/visualization/fig/cassava-0.1.0.png&quot; alt=&quot;Visualization&quot; width=&quot;500px&quot;&gt;&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/cassava" />
  <meta itemprop="sameAs" content="https://www.kaggle.com/c/cassava-disease/overview" />
  <meta itemprop="citation" content="@misc{mwebaze2019icassava,&#10;    title={iCassava 2019Fine-Grained Visual Categorization Challenge},&#10;    author={Ernest Mwebaze and Timnit Gebru and Andrea Frome and Solomon Nsumba and Jeremy Tusubira},&#10;    year={2019},&#10;    eprint={1908.02900},&#10;    archivePrefix={arXiv},&#10;    primaryClass={cs.CV}&#10;}" />
</div>

# `cassava`


*   **Visualization**:
    <a class="button button-with-icon" href="https://knowyourdata-tfds.withgoogle.com/#tab=STATS&dataset=cassava">
    Explore in Know Your Data
    <span class="material-icons icon-after" aria-hidden="true"> north_east
    </span> </a>

*   **Description**:

Cassava consists of leaf images for the cassava plant depicting healthy and four
(4) disease conditions; Cassava Mosaic Disease (CMD), Cassava Bacterial Blight
(CBB), Cassava Greem Mite (CGM) and Cassava Brown Streak Disease (CBSD). Dataset
consists of a total of 9430 labelled images. The 9430 labelled images are split
into a training set (5656), a test set(1885) and a validation set (1889). The
number of images per class are unbalanced with the two disease classes CMD and
CBSD having 72% of the images.

*   **Homepage**:
    [https://www.kaggle.com/c/cassava-disease/overview](https://www.kaggle.com/c/cassava-disease/overview)

*   **Source code**:
    [`tfds.image_classification.Cassava`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/image_classification/cassava.py)

*   **Versions**:

    *   **`0.1.0`** (default): No release notes.

*   **Download size**: `1.26 GiB`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split          | Examples
:------------- | -------:
`'test'`       | 1,885
`'train'`      | 5,656
`'validation'` | 1,889

*   **Features**:

```python
FeaturesDict({
    'image': Image(shape=(None, None, 3), dtype=tf.uint8),
    'image/filename': Text(shape=(), dtype=tf.string),
    'label': ClassLabel(shape=(), dtype=tf.int64, num_classes=5),
})
```

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('image', 'label')`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):

<img src="https://storage.googleapis.com/tfds-data/visualization/fig/cassava-0.1.0.png" alt="Visualization" width="500px">

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script src="https://www.gstatic.com/external_hosted/jquery2.min.js"></script>
<script>
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/cassava-0.1.0.html";
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
@misc{mwebaze2019icassava,
    title={iCassava 2019Fine-Grained Visual Categorization Challenge},
    author={Ernest Mwebaze and Timnit Gebru and Andrea Frome and Solomon Nsumba and Jeremy Tusubira},
    year={2019},
    eprint={1908.02900},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
```

