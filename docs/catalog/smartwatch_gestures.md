<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="smartwatch_gestures" />
  <meta itemprop="description" content="The **SmartWatch Gestures Dataset** has been collected to evaluate several gesture recognition algorithms for interacting with mobile applications using arm gestures.&#10;&#10;Eight different users performed twenty repetitions of twenty different gestures, for a total of 3200 sequences.&#10;Each sequence contains acceleration data from the 3-axis accelerometer of a first generation Sony SmartWatch™, as well as timestamps from the different clock sources available on an Android device.&#10;The smartwatch was worn on the user&#x27;s right wrist.&#10;The gestures have been manually segmented by the users performing them by tapping the smartwatch screen at the beginning and at the end of every repetition.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;smartwatch_gestures&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/smartwatch_gestures" />
  <meta itemprop="sameAs" content="https://tev.fbk.eu/technologies/smartwatch-gestures-dataset" />
  <meta itemprop="citation" content="@INPROCEEDINGS{&#10;  6952946,&#10;  author={Costante, Gabriele and Porzi, Lorenzo and Lanz, Oswald and Valigi, Paolo and Ricci, Elisa},&#10;  booktitle={2014 22nd European Signal Processing Conference (EUSIPCO)},&#10;  title={Personalizing a smartwatch-based gesture interface with transfer learning},&#10;  year={2014},&#10;  volume={},&#10;  number={},&#10;  pages={2530-2534},&#10;  doi={}}" />
</div>

# `smartwatch_gestures`


*   **Description**:

The **SmartWatch Gestures Dataset** has been collected to evaluate several
gesture recognition algorithms for interacting with mobile applications using
arm gestures.

Eight different users performed twenty repetitions of twenty different gestures,
for a total of 3200 sequences. Each sequence contains acceleration data from the
3-axis accelerometer of a first generation Sony SmartWatch™, as well as
timestamps from the different clock sources available on an Android device. The
smartwatch was worn on the user's right wrist. The gestures have been manually
segmented by the users performing them by tapping the smartwatch screen at the
beginning and at the end of every repetition.

*   **Homepage**:
    [https://tev.fbk.eu/technologies/smartwatch-gestures-dataset](https://tev.fbk.eu/technologies/smartwatch-gestures-dataset)

*   **Source code**:
    [`tfds.time_series.smartwatch_gestures.SmartwatchGestures`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/time_series/smartwatch_gestures/smartwatch_gestures.py)

*   **Versions**:

    *   **`1.0.0`** (default): Initial release.

*   **Download size**: `2.06 MiB`

*   **Dataset size**: `2.64 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Yes

*   **Splits**:

Split     | Examples
:-------- | -------:
`'train'` | 3,251

*   **Features**:

```python
FeaturesDict({
    'attempt': tf.uint8,
    'features': Sequence({
        'accel_x': tf.float64,
        'accel_y': tf.float64,
        'accel_z': tf.float64,
        'time_event': tf.uint64,
        'time_millis': tf.uint64,
        'time_nanos': tf.uint64,
    }),
    'gesture': ClassLabel(shape=(), dtype=tf.int64, num_classes=20),
    'participant': tf.uint8,
})
```

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('features', 'gesture')`

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
var url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/smartwatch_gestures-1.0.0.html";
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
@INPROCEEDINGS{
  6952946,
  author={Costante, Gabriele and Porzi, Lorenzo and Lanz, Oswald and Valigi, Paolo and Ricci, Elisa},
  booktitle={2014 22nd European Signal Processing Conference (EUSIPCO)},
  title={Personalizing a smartwatch-based gesture interface with transfer learning},
  year={2014},
  volume={},
  number={},
  pages={2530-2534},
  doi={}}
```

