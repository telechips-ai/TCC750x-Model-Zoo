
# TCC750x (N-Dolphin) Model Zoo
<a href="https://www.telechips.com/view/technology/prod04" target="_blank">
    <img src="./_docs/image/n_dolphin.png" alt="N-Dolphin Image">
</a> 

This repository provides a collection of neural network models optimized for Telechips AI SoC (TCC750x). 

The models are ready to run on evaluation boards and include benchmark results that show how the TCC750x performs.

---

## 1. Chip Description

### TCC750x (N-Dolphin)
- **Performance:** 4 + 4 TOPS  
- **Target Applications:**  
  - Advanced driver assistance systems (ADAS)
  - Vision-based applications (multi-camera processing)  
  - Driver Monitoring System (DMS)  
  - Deep learning inference

TCC750x offers real-time neural network inference capabilities with high efficiency and scalability for automotive applications. 

---

## 2. Overview of Overall Model Zoo
The following table summarizes the neural network models supported on TCC750x. Each model name links to its dedicated page with performance metrics and deployment instructions.

**Note**: The models covered in this document are based on original network architectures or have been minimally modified for compatibility with TCC750x execution. 
The results shown are not guaranteed for production use, and you are responsible for any further optimization.

### [Classification](Classification/README.md)
<table border="1" cellspacing="0" cellpadding="5" style="width:100%; table-layout:fixed;">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th rowspan="2">Accuracy</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="2">ConvMixer-768-32</td>
            <td align="center">224×224×3</td>
            <td align="center">133.05</td>
            <td align="center">0.484</td>
        </tr>
        <tr>
            <td align="center" colspan="2">EfficientNet-Lite0</td>
            <td align="center">224×224×3</td>
            <td align="center">1.26</td>
            <td align="center">0.711</td>
        </tr>
        <tr>
            <td align="center" rowspan="3" colspan="2">EfficientNet-v2s</td>
            <td align="center">224×224×3</td>
            <td align="center">11.15</td>
            <td align="center">0.461</td>
        </tr>
        <tr>
            <td align="center">640×320×3</td>
            <td align="center">39.25</td>
            <td align="center">0.673</td>
        </tr>
        <tr>
            <td align="center">960×520×3</td>
            <td align="center">74.96</td>
            <td align="center">0.688</td>
        </tr>
        <tr>
            <td align="center" colspan="2">LeNet5</td>
            <td align="center">32×32×1</td>
            <td align="center">0.05</td>
            <td align="center">0.982</td>
        </tr>
        <tr>
            <td align="center" colspan="2">MobileNet-v2-10</td>
            <td align="center">224×224×3</td>
            <td align="center">1.24</td>
            <td align="center">0.688</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" colspan="2">MobileOne-s1</td>
            <td align="center">640×320×3</td>
            <td align="center">4.7</td>
            <td align="center">0.522</td>
        </tr>
        <tr>
            <td align="center">960×520×3</td>
            <td align="center">13.04</td>
            <td align="center">0.542</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" colspan="2">RegNetX-400mf</td>
            <td align="center">640×320×3</td>
            <td align="center">7.17</td>
            <td align="center">0.524</td>
        </tr>
        <tr>
            <td align="center">960×520×3</td>
            <td align="center">15.95</td>
            <td align="center">0.57</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" colspan="2">ResNet-18</td>
            <td align="center">640×320×3</td>
            <td align="center">15.34</td>
            <td align="center">0.586</td>
        </tr>
        <tr>
            <td align="center">960×520×3</td>
            <td align="center">36.01</td>
            <td align="center">0.605</td>
        </tr>
        <tr>
            <td align="center" rowspan="3" colspan="2">ResNet-50</td>
            <td align="center">224×224×3</td>
            <td align="center">9.09</td>
            <td align="center">0.716</td>
        </tr>
        <tr>
            <td align="center">640×320×3</td>
            <td align="center">29.95</td>
            <td align="center">0.619</td>
        </tr>
        <tr>
            <td align="center">960×520×3</td>
            <td align="center">77.52</td>
            <td align="center">0.65</td>
        </tr>
        <tr>
            <td align="center" colspan="2">ResNet-50-v2</td>
            <td align="center">224×224×3</td>
            <td align="center">9.84</td>
            <td align="center">0.677</td>
        </tr>
    </tbody>
</table>

### [Object Detection](Object_Detection/README.md)
<table border="1" cellspacing="0" cellpadding="5" style="width:100%; table-layout:fixed;">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th rowspan="2">mAP@50</th>
        </tr>
    </thead>      
        <tr>
            <td align="center" colspan="2">SSDlite-MobileNet-v1</td> <!-- Model -->
            <td align="center">320x320x3</td> <!-- Input Size(WxHxC) -->
            <td align="center">2.46</td> <!-- Inference Time(msec): EVB -->
            <td align="center">0.367</td> <!-- COCO AP@[.50:.95] -->
        </tr>
        <tr>
            <td align="center" colspan="2">SSDlite-MobileNet-v2</td> <!-- Model -->
            <td align="center">300x300x3</td> <!-- Input Size(WxHxC) -->
            <td align="center">2.00</td> <!-- Inference Time(msec): EVB -->
            <td align="center">0.651</td> <!-- Evaluation Result: INT8 -->
        </tr>
        <tr>
            <td align="center" colspan="2">YOLOv3</td> <!-- Model -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">63.60</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.598</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" colspan="2">YOLOv4</td> <!-- Model -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">57.50</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.735</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv5</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">8.97</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.383</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">13.74</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.509</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">32.96</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.584</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">54.01</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.619</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">104.11</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.643</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model">YOLOv6</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">6.50</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.493</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">20.43</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.552</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">36.80</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.643</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">67.35</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.673</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="2">YOLOv7</td> <!-- Model -->
            <td align="center" class="variant">-</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">50.21</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.648</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">tiny</td>
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">9.84</td>
            <td align="center">0.459</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">8.09</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.488</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">15.49</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.576</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">39.31</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.632</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">67.04</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.654</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">113.31</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.664</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model">YOLOv9</td>
            <td align="center" class="variant">s</td>
            <td align="center">640x640x3</td>
            <td align="center">77.34</td>
            <td align="center">0.551</td>
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model">YOLOX</td> <!-- Models -->
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">24.52</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.467</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">49.35</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.536</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">77.11</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.565</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">136.51</td> <!-- Inference Time (ms/img) -->
            <td align="center">0.583</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">tiny</td> <!-- Models: Variant -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">8.53</td> <!-- Inference Time (ms/img) -->
            <td align="center">0.401</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">nano</td> <!-- Models: Variant -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">6.09</td> <!-- Inference Time (ms/img) -->
            <td align="center">0.112</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
    </tbody>
</table>


### [Segmentation](Segmentation/README.md)
<table border="1" cellspacing="0" cellpadding="5" style="width:100%; table-layout:fixed;">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th rowspan="2">BBox mAP@50</th>
            <th rowspan="2">Mask mAP@50</th>
        </tr>
    </thead>   
        <tr>
            <td align="center" rowspan="4" class="model">YOLOv11-Seg</td> <!-- Models -->
            <td align="center" class="variant" rowspan="2">m</td> <!-- Models: Variant -->
            <td align="center">512x512x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">37.5</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.579</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">0.518</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">62.9</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.597</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">0.54</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant" rowspan="2">l</td> <!-- Models: Variant -->
            <td align="center">512x512x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">44.4</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.594</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">0.532</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="center">73.7</td> <!-- Inference Time (msec): EVB -->
            <td align="center">0.616</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">0.556</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        </tr>
    </tbody>
</table>


## **3. Getting Started**
Follow these steps to run a model provided by Telechips Model Zoo on the TCC750x Evaluation Board (EVB).

### 1. Clone the repository:
<pre> <code>
git clone git@github.com:telechips-ai/TCC750x-Model-Zoo.git
</code> </pre>

### 2. Copy the desired model to the EVB:
Copy the entire model folder (yolov5m) to the TCC750x EVB.  
You can either copy the folder as it is or rename it to yolov5m_quantized to match the format used in previously released neural network folders, as shown in the following example.  
Each folder contains the necessary output files (.so and .bin).
<pre> <code>
scp -r [network_output_folder] root@192.168.0.100:/path/to/target/
</code> </pre>
Replace [network_output_folder] with the actual folder (e.g., yolov5m/).  

### ***Example: TCC750x - YOLOv5m Folder Structure***
<pre> <code>
yolov5m/
├── net.so        # Compiled model library
├── npu_cmd.bin       # Binary file of TCC750x NPU command code word
└── quantized_network.bin # Binary file of Quantized weight and bias 
</code> </pre>
Then run:
<pre> <code>
scp -r yolov5m_quantized/ root@192.168.0.100:/home/root/
</code> </pre>

### 3. Run the model using tcnputestapp or tcnnapp:
<pre> <code>
tcnputestapp -d 0 1 -n [network_output_folder_path]
</code> </pre>
or
<pre> <code>
tcnnapp -n [network_output_folder_path]
</code> </pre>
