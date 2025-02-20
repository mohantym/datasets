<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="bee_dataset" />
  <meta itemprop="description" content="This dataset contains images and a set of labels that expose certain characterisitics of that images, such as *varroa-mite* infections, bees carrying *pollen-packets* or bee that are *cooling the hive* by flappingn their wings. Additionally, this dataset contains images of *wasps* to be able to distinguish bees and wasps.&#10;&#10;The images of the bees are taken from above and rotated. The bee is vertical and either its head or the trunk is on top. All images were taken with a green background and the distance to the bees was always the same, thus all bees have the same size.&#10;&#10;Each image can have multiple labels assigned to it. E.g. a bee can be cooling the hive and have a varrio-mite infection at the same time.&#10;&#10;This dataset is designed as mutli-label dataset, where each label, e.g. *varroa_output*, contains 1 if the characterisitic was present in the image and a 0 if it wasn&#x27;t. All images are provided by 300 pixel height and 150 pixel witdh. As default the dataset provides the images as 150x75 (h,w) pixel. You can select 300 pixel height by loading the datset with the name &quot;bee_dataset/bee_dataset_300&quot; and with 200 pixel height by &quot;bee_dataset/bee_dataset_200&quot;.&#10;&#10;License: GNU GENERAL PUBLIC LICENSE&#10;&#10;Author: Fabian Hickert &lt;Fabian.Hickert@raspbee.de&gt;&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;bee_dataset&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;&lt;img src=&quot;https://storage.googleapis.com/tfds-data/visualization/fig/bee_dataset-bee_dataset_300-1.0.0.png&quot; alt=&quot;Visualization&quot; width=&quot;500px&quot;&gt;&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/bee_dataset" />
  <meta itemprop="sameAs" content="https://raspbee.de" />
  <meta itemprop="citation" content="@misc{BeeAlarmed - A camera based bee-hive monitoring,&#10;  title =   &quot;Dataset for a camera based bee-hive monitoring&quot;,&#10;  url={https://github.com/BeeAlarmed}, journal={BeeAlarmed},&#10;  author =  &quot;Fabian Hickert&quot;,&#10;  year   =  &quot;2021&quot;,&#10;  NOTE   = &quot;\url{https://raspbee.de/} and \url{https://github.com/BeeAlarmed/BeeAlarmed}&quot;&#10;}" />
</div>

# `bee_dataset`


*   **Description**:

This dataset contains images and a set of labels that expose certain
characterisitics of that images, such as *varroa-mite* infections, bees carrying
*pollen-packets* or bee that are *cooling the hive* by flappingn their wings.
Additionally, this dataset contains images of *wasps* to be able to distinguish
bees and wasps.

The images of the bees are taken from above and rotated. The bee is vertical and
either its head or the trunk is on top. All images were taken with a green
background and the distance to the bees was always the same, thus all bees have
the same size.

Each image can have multiple labels assigned to it. E.g. a bee can be cooling
the hive and have a varrio-mite infection at the same time.

This dataset is designed as mutli-label dataset, where each label, e.g.
*varroa_output*, contains 1 if the characterisitic was present in the image and
a 0 if it wasn't. All images are provided by 300 pixel height and 150 pixel
witdh. As default the dataset provides the images as 150x75 (h,w) pixel. You can
select 300 pixel height by loading the datset with the name
"bee_dataset/bee_dataset_300" and with 200 pixel height by
"bee_dataset/bee_dataset_200".

License: GNU GENERAL PUBLIC LICENSE

Author: Fabian Hickert <Fabian.Hickert@raspbee.de>

*   **Homepage**: [https://raspbee.de](https://raspbee.de)

*   **Source code**:
    [`tfds.image_classification.bee_dataset.BeeDataset`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/image_classification/bee_dataset/bee_dataset.py)

*   **Versions**:

    *   **`1.0.0`** (default): No release notes.

*   **Download size**: `192.39 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Yes

*   **Splits**:

Split     | Examples
:-------- | -------:
`'train'` | 7,490

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('input', 'output')`

*   **Citation**:

```
@misc{BeeAlarmed - A camera based bee-hive monitoring,
  title =   "Dataset for a camera based bee-hive monitoring",
  url={https://github.com/BeeAlarmed}, journal={BeeAlarmed},
  author =  "Fabian Hickert",
  year   =  "2021",
  NOTE   = "\url{https://raspbee.de/} and \url{https://github.com/BeeAlarmed/BeeAlarmed}"
}
```


## bee_dataset/bee_dataset_300 (default config)

*   **Config description**: BeeDataset images with 300 pixel height and 150
    pixel width

*   **Dataset size**: `97.96 MiB`

*   **Features**:

```python
FeaturesDict({
    'input': Image(shape=(300, 150, 3), dtype=tf.uint8),
    'output': FeaturesDict({
        'cooling_output': tf.float64,
        'pollen_output': tf.float64,
        'varroa_output': tf.float64,
        'wasps_output': tf.float64,
    }),
})
```

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):

<img src="https://storage.googleapis.com/tfds-data/visualization/fig/bee_dataset-bee_dataset_300-1.0.0.png" alt="Visualization" width="500px">

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script src="https://www.gstatic.com/external_hosted/jquery2.min.js"></script>
<script>
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/bee_dataset-bee_dataset_300-1.0.0.html";
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

## bee_dataset/bee_dataset_200

*   **Config description**: BeeDataset images with 200 pixel height and 100
    pixel width

*   **Dataset size**: `55.48 MiB`

*   **Features**:

```python
FeaturesDict({
    'input': Image(shape=(200, 100, 3), dtype=tf.uint8),
    'output': FeaturesDict({
        'cooling_output': tf.float64,
        'pollen_output': tf.float64,
        'varroa_output': tf.float64,
        'wasps_output': tf.float64,
    }),
})
```

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):

<img src="https://storage.googleapis.com/tfds-data/visualization/fig/bee_dataset-bee_dataset_200-1.0.0.png" alt="Visualization" width="500px">

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script src="https://www.gstatic.com/external_hosted/jquery2.min.js"></script>
<script>
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/bee_dataset-bee_dataset_200-1.0.0.html";
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

## bee_dataset/bee_dataset_150

*   **Config description**: BeeDataset images with 200 pixel height and 100
    pixel width

*   **Dataset size**: `37.43 MiB`

*   **Features**:

```python
FeaturesDict({
    'input': Image(shape=(150, 75, 3), dtype=tf.uint8),
    'output': FeaturesDict({
        'cooling_output': tf.float64,
        'pollen_output': tf.float64,
        'varroa_output': tf.float64,
        'wasps_output': tf.float64,
    }),
})
```

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):

<img src="https://storage.googleapis.com/tfds-data/visualization/fig/bee_dataset-bee_dataset_150-1.0.0.png" alt="Visualization" width="500px">

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script src="https://www.gstatic.com/external_hosted/jquery2.min.js"></script>
<script>
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/bee_dataset-bee_dataset_150-1.0.0.html";
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