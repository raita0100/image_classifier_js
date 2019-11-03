# image_classifier_js
> this project contains how to use pre trained models using tensorflow api in the web browser
 </br>
 
 ## scripts for loading the tensorflow in javascript
 ```
 <!-- Load the latest version of TensorFlow.js -->
    <script src="https://unpkg.com/@tensorflow/tfjs"></script>
    <script src="https://unpkg.com/@tensorflow-models/mobilenet"></script>
    <script src="https://unpkg.com/@tensorflow-models/knn-classifier"></script>
 ```
 
### 1. Initializing the classifier.
```sh
const classifier = knnClassifier.create();
```

### 2.Load the mobilenet.

```
// Load the model.
net = await mobilenet.load();
```

### 3. get the activation
```
// Get the activation from mobilenet from the webcam.
const activation = net.infer(webcamElement, 'conv_preds');
```

### 4. Make the prediction
```
 // Get the most likely class and confidences from the classifier module.
 const result = await classifier.predictClass(activation);
```
