# YOLO Series Benchmark on TCC750x

The following table shows benchmark results for various YOLO object detection models running on the TCC750x NPU.  
YOLO models are widely known for their real-time performance and high accuracy in detecting multiple objects in a single pass over the image.

Click on the model name to download a tar file containing the model binary for TCC750x.

**Note**: YOLO stands for You Only Look Once.

---


![YOLO Model Performance](../../_docs/image/yolo_performance.png)

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model     |
| **Framework**            | Deep learning framework used (e.g., PyTorch\*, TFLite, ONNX)                   |
| **Dataset**              | Dataset used to benchmark model performance                                 |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the N-Dolphin EVB by using zero-padded input images                             |
| **mAP**             | Mean Average Precision (mAP) is evaluated on the **COCO2017 validation dataset** (5,000 images)                    |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: Weight and Bias Binary (.bin) and Command Binary (.bin) for execution on TCC750x                    |
| **References**           | Link to the original repository of the model                         |

---



<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th align="center" rowspan="2" colspan="2">Model</th>
            <th th align="center" rowspan="2">Framework</th>
            <th th align="center" rowspan="2">Dataset</th>
            <th th align="center" rowspan="2">Input Size (WxHxC)</th>
            <th align="center" rowspan="2">Inference Time (ms)</th>
            <th align="center" colspan="2">mAP@50:95</th>
            <th align="center" colspan="2">mAP@50</th>
            <th align="center" rowspan="2">Quantization Bit</th>
            <th align="center" colspan="2">Compiled Model Files</th>
            <th align="center" rowspan="2">References</th>
        </tr>
        <tr>
            <th>FP32</th>
            <th>INT8</th>
            <th>FP32</th>
            <th>INT8</th>
            <th>Weight and Bias Binary (MB)</th>
            <th>Command Binary (KB)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="2"><a href="./yolov3/yolov3/">YOLOv3</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">63.6</td>
            <td align="center">0.439</td>
            <td align="center">0.386</td>
            <td align="center">0.63</td>
            <td align="center">0.598</td>
            <td align="center">INT8 </td>
            <td align="center">60.55</td>
            <td align="center">230</td>
            <td align="center"><a href="https://github.com/ultralytics/yolov3">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" colspan="2"><a href="./yolov4/yolov4/">YOLOv4</a></td> <!-- Model -->
            <td align="center">Darknet</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">57.5</td>
            <td align="center">0.501</td>
            <td align="center">0.402</td>
            <td align="center">0.748</td>
            <td align="center">0.735</td>
            <td align="center">INT8 </td>
            <td align="center">62.92</td>
            <td align="center">306</td>
            <td align="center"><a href="https://github.com/AlexeyAB/darknet/blob/master/cfg/yolov4.cfg">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv5</td> <!-- Model -->
            <td align="center" class="variant"><a href="./yolov5/yolov5n/">n</a></td>
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">8.97</td>
            <td align="center">0.246</td>
            <td align="center">0.213</td>
            <td align="center">0.418</td>
            <td align="center">0.383</td>
            <td align="center">INT8 </td>
            <td align="center">1.86</td>
            <td align="center">78</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/yolov5">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov5/yolov5s/">s</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">13.74</td>
            <td align="center">0.342</td>
            <td align="center">0.303</td>
            <td align="center">0.533</td>
            <td align="center">0.509</td>
            <td align="center">INT8 </td>
            <td align="center">7.12</td>
            <td align="center">142</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov5/yolov5m/">m</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">32.96</td>
            <td align="center">0.424</td>
            <td align="center">0.385</td>
            <td align="center">0.61</td>
            <td align="center">0.584</td>
            <td align="center">INT8 </td>
            <td align="center">20.81</td>
            <td align="center">185</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov5/yolov5l/">l</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">54.01</td>
            <td align="center">0.461</td>
            <td align="center">0.406</td>
            <td align="center">0.644</td>
            <td align="center">0.619</td>
            <td align="center">INT8 </td>
            <td align="center">45.6</td>
            <td align="center">305</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov5/yolov5x/">x</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">104.11</td>
            <td align="center">0.478</td>
            <td align="center">0.437</td>
            <td align="center">0.66</td>
            <td align="center">0.643</td>
            <td align="center">INT8 </td>
            <td align="center">84.97</td>
            <td align="center">459</td>
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model">YOLOv6</td> <!-- Model -->
            <td align="center" class="variant"><a href="./yolov6/yolov6n/">n</a></td> <!-- Models: Variant -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">6.5</td>
            <td align="center">0.353</td>
            <td align="center">0.332</td>
            <td align="center">0.514</td>
            <td align="center">0.493</td>
            <td align="center">INT8 </td>
            <td align="center">4.56</td>
            <td align="center">37</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov6/yolov6s/">s</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">20.43</td>
            <td align="center">0.422</td>
            <td align="center">0.384</td>
            <td align="center">0.597</td>
            <td align="center">0.552</td>
            <td align="center">INT8 </td>
            <td align="center">18.14</td>
            <td align="center">83</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov6/yolov6m/">m</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">36.8</td>
            <td align="center">0.468</td>
            <td align="center">0.462</td>
            <td align="center">0.648</td>
            <td align="center">0.643</td>
            <td align="center">INT8 </td>
            <td align="center">34.12</td>
            <td align="center">113</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov6/yolov6l/">l</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">67.35</td>
            <td align="center">0.496</td>
            <td align="center">0.489</td>
            <td align="center">0.683</td>
            <td align="center">0.673</td>
            <td align="center">INT8 </td>
            <td align="center">58.31</td>
            <td align="center">237</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model">YOLOv7</td> <!-- Model -->
            <td align="center" class="variant"><a href="./yolov7/yolov7/">-</a></td>
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">50.21</td>
            <td align="center">0.479</td>
            <td align="center">0.421</td>
            <td align="center">0.662</td>
            <td align="center">0.648</td>
            <td align="center">INT8 </td>
            <td align="center">36.11</td>
            <td align="center">242</td>
            <td align="center" rowspan="2"><a href="https://github.com/WongKinYiu/yolov7">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov7/yolov7_tiny/">tiny</a></td>
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">9.84</td>
            <td align="center">0.154</td>
            <td align="center">0.136</td>
            <td align="center">0.488</td>
            <td align="center">0.459</td>
            <td align="center">INT8 </td>
            <td align="center">6.11</td>
            <td align="center">59</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Model -->
            <td align="center" class="variant"><a href="./yolov8/yolov8n/">n</a></td>
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">8.09</td>
            <td align="center">0.344</td>
            <td align="center">0.331</td>
            <td align="center">0.501</td>
            <td align="center">0.488</td>
            <td align="center">INT8 </td>
            <td align="center">3.15</td>
            <td align="center">70</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov8/yolov8s/">s</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">15.49</td>
            <td align="center">0.416</td>
            <td align="center">0.405</td>
            <td align="center">0.586</td>
            <td align="center">0.576</td>
            <td align="center">INT8 </td>
            <td align="center">10.93</td>
            <td align="center">91</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov8/yolov8m/">m</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">39.31</td>
            <td align="center">0.472</td>
            <td align="center">0.458</td>
            <td align="center">0.644</td>
            <td align="center">0.632</td>
            <td align="center">INT8 </td>
            <td align="center">25.39</td>
            <td align="center">153</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov8/yolov8l/">l</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">67.04</td>
            <td align="center">0.499</td>
            <td align="center">0.483</td>
            <td align="center">0.67</td>
            <td align="center">0.654</td>
            <td align="center">INT8 </td>
            <td align="center">42.72</td>
            <td align="center">245</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yolov8/yolov8x/">x</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">113.31</td>
            <td align="center">0.508</td>
            <td align="center">0.493</td>
            <td align="center">0.681</td>
            <td align="center">0.664</td>
            <td align="center">INT8 </td>
            <td align="center">66.85</td>
            <td align="center">434</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model">YOLOv9</td> <!-- Model -->
            <td align="center" class="variant"><a href="./yolov9/yolov9s/">s</a></td>
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">77.34</td>
            <td align="center">0.414</td>
            <td align="center">0.404</td>
            <td align="center">0.562</td>
            <td align="center">0.551</td>
            <td align="center">INT8 </td>
            <td align="center">7.343</td>
            <td align="center">132</td>
            <td align="center" rowspan="1"><a href="https://github.com/ultralytics/ultralytics">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model">YOLOX</td> <!-- Model -->
            <td align="center" class="variant"><a href="./yoloX/yolox_s/">s</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">24.52</td>
            <td align="center">0.316</td>
            <td align="center">0.308</td>
            <td align="center">0.473</td>
            <td align="center">0.467</td>
            <td align="center">INT8 </td>
            <td align="center">8.82</td>
            <td align="center">186</td>
            <td align="center" rowspan="6"><a href="https://github.com/Megvii-BaseDetection/YOLOX">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yoloX/yolox_m/">m</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">49.35</td>
            <td align="center">0.382</td>
            <td align="center">0.371</td>
            <td align="center">0.542</td>
            <td align="center">0.536</td>
            <td align="center">INT8 </td>
            <td align="center">24.86</td>
            <td align="center">235</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yoloX/yolox_l/">l</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">77.11</td>
            <td align="center">0.414</td>
            <td align="center">0.403</td>
            <td align="center">0.572</td>
            <td align="center">0.565</td>
            <td align="center">INT8 </td>
            <td align="center">53.08</td>
            <td align="center">370</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yoloX/yolox_x/">x</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">136.51</td>
            <td align="center">0.432</td>
            <td align="center">0.418</td>
            <td align="center">0.591</td>
            <td align="center">0.583</td>
            <td align="center">INT8 </td>
            <td align="center">97.01</td>
            <td align="center">558</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yoloX/yolox_tiny/">tiny</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">8.53</td>
            <td align="center">0.265</td>
            <td align="center">0.255</td>
            <td align="center">0.411</td>
            <td align="center">0.401</td>
            <td align="center">INT8 </td>
            <td align="center">5.04</td>
            <td align="center">61</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="./yoloX/yolox_nano/">nano</a></td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">6.09</td>
            <td align="center">0.201</td>
            <td align="center">0.063</td>
            <td align="center">0.326</td>
            <td align="center">0.112</td>
            <td align="center">INT8 </td>
            <td align="center">0.93</td>
            <td align="center">62</td>
        </tr>
    </tbody>
</table>


## 📤 Output Format

- The raw output of a YOLO model is a tensor (or multiple tensors) containing a dense grid of predictions across different spatial locations and anchor boxes.
- These raw outputs undergo post-processing, which includes:
  - Applying sigmoid/softmax activations to normalize outputs
  - Filtering boxes based on confidence thresholds
  - Applying Non-maximum Suppression (NMS) to remove overlapping boxes

- The final post-processed output includes a list of detected objects, each containing:
  - Class label
  - Confidence score
  - Bounding box coordinates (x_min, y_min, x_max, and y_max)

- The number and format of output tensors may vary slightly depending on the YOLO version (e.g., v5, v6, v8, and YOLOX), but the core structure remains similar.

### Footnote                
* PyTorch* models are converted to ONNX for deployment.
