# YOLOv8 Benchmark on TCC750x
![YOLO Model Performance](../../../_docs/image/yolov8_performance.png)
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
            <th align="center" colspan="2">References</th>
        </tr>
        <tr>
            <th>FP32</th>
            <th>INT8</th>
            <th>FP32</th>
            <th>INT8</th>
            <th>Weight and Bias Binary (MB)</th>
            <th>Command Binary (KB)</th>
            <th>Link</th>
            <th>License</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Model -->
            <td align="center" class="variant">n</td>
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">8.09</td>
            <td align="right">0.344</td>
            <td align="right">0.331</td>
            <td align="right">0.501</td>
            <td align="right">0.488</td>
            <td align="center">INT8 </td>
            <td align="right">3.15</td>
            <td align="right">70</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub<a></td> <!-- References: Link -->
            <td align="center" rowspan="5">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">15.49</td>
            <td align="right">0.416</td>
            <td align="right">0.405</td>
            <td align="right">0.586</td>
            <td align="right">0.576</td>
            <td align="center">INT8 </td>
            <td align="right">10.93</td>
            <td align="right">91</td>
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">39.31</td>
            <td align="right">0.472</td>
            <td align="right">0.458</td>
            <td align="right">0.644</td>
            <td align="right">0.632</td>
            <td align="center">INT8 </td>
            <td align="right">25.39</td>
            <td align="right">153</td>
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">67.04</td>
            <td align="right">0.499</td>
            <td align="right">0.483</td>
            <td align="right">0.67</td>
            <td align="right">0.654</td>
            <td align="center">INT8 </td>
            <td align="right">42.72</td>
            <td align="right">245</td>
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Model -->
            <td align="center">PyTorch</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">113.31</td>
            <td align="right">0.508</td>
            <td align="right">0.493</td>
            <td align="right">0.681</td>
            <td align="right">0.664</td>
            <td align="center">INT8 </td>
            <td align="right">66.85</td>
            <td align="right">434</td>
        </tr>
    </tbody>
</table>
