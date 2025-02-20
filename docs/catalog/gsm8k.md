<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="gsm8k" />
  <meta itemprop="description" content="A dataset of 8.5K high quality linguistically diverse grade school math word problems.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;gsm8k&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/gsm8k" />
  <meta itemprop="sameAs" content="https://github.com/openai/grade-school-math" />
  <meta itemprop="citation" content="@misc{cobbe2021training,&#10;      title={Training Verifiers to Solve Math Word Problems},&#10;      author={Karl Cobbe and Vineet Kosaraju and Mohammad Bavarian and Jacob Hilton and Reiichiro Nakano and Christopher Hesse and John Schulman},&#10;      year={2021},&#10;      eprint={2110.14168},&#10;      archivePrefix={arXiv},&#10;      primaryClass={cs.LG}&#10;}" />
</div>

# `gsm8k`


*   **Description**:

A dataset of 8.5K high quality linguistically diverse grade school math word
problems.

*   **Homepage**:
    [https://github.com/openai/grade-school-math](https://github.com/openai/grade-school-math)

*   **Source code**:
    [`tfds.text.gsm8k.Gsm8k`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/text/gsm8k/gsm8k.py)

*   **Versions**:

    *   **`1.0.0`** (default): Initial release.

*   **Download size**: `10.77 MiB`

*   **Dataset size**: `17.84 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Yes

*   **Splits**:

Split              | Examples
:----------------- | -------:
`'test'`           | 1,319
`'test_socratic'`  | 1,319
`'train'`          | 7,473
`'train_socratic'` | 7,473

*   **Features**:

```python
FeaturesDict({
    'annotation': Text(shape=(), dtype=tf.string),
    'answer': Text(shape=(), dtype=tf.string),
    'question': Text(shape=(), dtype=tf.string),
    'short_answer': Text(shape=(), dtype=tf.string),
})
```

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `None`

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
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/gsm8k-1.0.0.html";
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
@misc{cobbe2021training,
      title={Training Verifiers to Solve Math Word Problems},
      author={Karl Cobbe and Vineet Kosaraju and Mohammad Bavarian and Jacob Hilton and Reiichiro Nakano and Christopher Hesse and John Schulman},
      year={2021},
      eprint={2110.14168},
      archivePrefix={arXiv},
      primaryClass={cs.LG}
}
```

