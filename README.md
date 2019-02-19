# My first App using Tensorflow LITE


- **Installation** 

```
pip install --upgrade "tensorflow==1.9"
```
- **if you are on WINDOWS there are some limitations for tflite_converter**
follow [this](https://stackoverflow.com/a/53190791/9329562) or you can follow [this](https://stackoverflow.com/a/51771078/9329562)


**Clone the github repo**
```
git clone https://github.com/googlecodelabs/tensorflow-for-poets-2

cd tensorflow-for-poets-2
```

**Download The training data**

```
wget http://download.tensorflow.org/example_images/flower_photos.tgz

tar -xf flower_photos.tgz
```


- **To convert a GrapgDef to .tflite**
```
tflite_convert \
  --output_file=/tmp/foo.tflite \
  --graph_def_file=/tmp/mobilenet_v1_0.50_128/frozen_graph.pb \
  --input_arrays=input \
  --output_arrays=MobilenetV1/Predictions/Reshape_1
 ```
