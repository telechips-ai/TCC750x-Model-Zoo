# Classification Benchmark on TCC750x
The following table shows benchmark results for various classification models running on the TCC750x NPU.
You can compare the performance of each model.

Click on the model name to download a tar file containing the model binary for TCC750x.

- - -
![classification Model Performance](../_docs/image/cls_performance.png)
### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model     |
| **Framework**            | Deep learning framework used (e.g., PyTorch\*, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance  |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC750x EVB using zero-padded input images                |
| **Accuracy**             | Top-1 classification accuracy on the validation dataset                     |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: Weight and Bias Binary (.bin) and Command Binary (.bin) for execution on TCC750x                    |
| **References**           | Link to the original repository of the model

- - -

<table border="1" cellspacing="0" cellpadding="5">
    <thead>
    <tr>
        <th rowspan="2" colspan="2">Model</th>
        <th rowspan="2">Framework</th>
        <th rowspan="2">Dataset</th>
        <th rowspan="2">Input Size (WxHxC)</th>
        <th rowspan="2">Inference Time (ms)</th>
        <th colspan="2">Accuracy</th>
        <th rowspan="2">Quantization Bit</th>
        <th colspan="2">Compiled Model Files</th>
        <th rowspan="2">References</th>
    </tr>
    <tr>
        <th>FP32</th>
        <th>INT8</th>
        <th>Weight and Bias Binary Size (MB)</th>
        <th>Command Binary Size (KB)</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="1"><a href="ConvMixer/README.md">ConvMixer</a></td>
            <td align="center" rowspan="1" class="variant"><a href="ConvMixer/convmixer_768_32/">768-32</a></td>
            <td align="center">PyTorch </td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">133.05</td>
            <td align="right">0.531</td>
            <td align="right">0.484</td>
            <td align="center">INT8 </td>
            <td align="right">21.00</td>
            <td align="right">966</td>
            <td align="center"><a href="https://huggingface.co/timm/convmixer_768_32.in1k">Hugging Face</a></td>
        </tr>
        <tr>
            <td align="center" colspan="1"><a href="EfficientNet/README.md">EfficientNet</td>
            <td align="center" rowspan="1" class="variant"><a href="EfficientNet/efficientnet_lite0/">Lite0</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">1.26</td>
            <td align="right">0.714</td>
            <td align="right">0.711</td>
            <td align="center">INT8 </td>
            <td align="right">4.67</td>
            <td align="right">22</td>
            <td align="center"><a href="https://huggingface.co/timm/efficientnet_lite0.ra_in1k">Hugging Face</a></td>
        </tr>
        <tr>
            <td align="center" colspan="1" rowspan="3"><a href="EfficientNet/README.md">EfficientNet-v2</td>
            <td align="center" rowspan="3" class="variant"><a href="EfficientNet/efficientnet_v2s/">s</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">11.15</td>
            <td align="right">0.782</td>
            <td align="right">0.461</td>
            <td align="center">INT8 </td>
            <td align="right">21.54</td>
            <td align="right">364</td>
            <td align="center" rowspan="3" class="variant"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.efficientnet_v2_s.html#torchvision.models.EfficientNet_V2_S_Weights">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">640x320x3</td>
            <td align="right">39.25</td>
            <td align="right">0.695</td>
            <td align="right">0.673</td>
            <td align="center">INT8 </td>
            <td align="right">21.04</td>
            <td align="right">445</td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">960x520x3</td>
            <td align="right">74.96</td>
            <td align="right">0.724</td>
            <td align="right">0.688</td>
            <td align="center">INT8 </td>
            <td align="right">21.04</td>
            <td align="right">753</td>
        </tr>
        <tr>
            <td align="center" colspan="2"><a href="LeNet5/README.md">LeNet5</a></td>
            <td align="center">PyTorch</td>
            <td align="center">MNIST</td>
            <td align="center">32x32x1</td>
            <td align="right">0.05</td>
            <td align="right">0.986</td>
            <td align="right">0.982</td>
            <td align="center">INT8 </td>
            <td align="right">0.05</td>
            <td align="right">2</td>
            <td align="center"><a href="https://huggingface.co/mindspore-ai/LeNet">Hugging Face</a></td>
        </tr>
        <tr>
            <td align="center" colspan="1" rowspan="1"><a href="MobileNet/README.md">MobileNet-v2</a></td>
            <td align="center" colspan="1"><a href="MobileNet/mobilenet_v2_10/">10</a></td>
            <td align="center">MXNet</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">0.97</td>
            <td align="right">0.698</td>
            <td align="right">0.688</td>
            <td align="center">INT8</td>
            <td align="right">3.47</td>
            <td align="right">41</td>
            <td align="center"><a href="https://github.com/onnx/models/tree/main/validated/vision/classification/mobilenet">GitHub</a></td>
        </tr>
        <tr>
            <td align="center" rowspan="2" colspan="1"><a href="MobileOne/README.md">MobileOne</a></td>
            <td align="center" rowspan="2" class="variant"><a href="MobileOne/mobileone_s1/">s1</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">640x320x3</td>
            <td align="right">4.70</td>
            <td align="right">0.556</td>
            <td align="right">0.522</td>
            <td align="center">INT8 </td>
            <td align="right">4.61</td>
            <td align="right">134</td>
            <td align="center" rowspan="2" class="variant"><a href="https://huggingface.co/timm/mobileone_s1.apple_in1k">Hugging Face</a></td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">960x520x3</td>
            <td align="right">13.04</td>
            <td align="right">0.575</td>
            <td align="right">0.542</td>
            <td align="center">INT8 </td>
            <td align="right">4.61</td>
            <td align="right">134</td>
        </tr>
        <tr>
            <td align="center" rowspan="3" colspan="1"><a href="RegNet/README.md">RegNetX</a></td>
            <td align="center" rowspan="2" colspan="1"><a href="RegNet/regnetx_400mf/">400mf</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">640x320x3</td>
            <td align="right">7.17</td>
            <td align="right">0.529</td>
            <td align="right">0.524</td>
            <td align="center">INT8 </td>
            <td align="right">23.37</td>
            <td align="right">32</td>
            <td align="center" rowspan="2" colspan="1"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.regnet_y_400mf.html#torchvision.models.regnet_y_400mf">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">960x520x3</td>
            <td align="right">15.95</td>
            <td align="right">0.575</td>
            <td align="right">0.570</td>
            <td align="center">INT8 </td>
            <td align="right">23.37</td>
            <td align="right">47</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" colspan="1"><a href="regnetx_800mf/">800mf</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">4.81</td>
            <td align="right">0.733</td>
            <td align="right">0.731</td>
            <td align="center">INT8 </td>
            <td align="right">30.99</td>
            <td align="right">29</td>
            <td align="center" rowspan="1" colspan="1"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.regnet_x_800mf.html#torchvision.models.regnet_x_800mf">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center" rowspan="9" class="model"><a href="ResNet/README.md">ResNet</a></td>
            <td align="center" rowspan="2" class="variant"><a href="ResNet/resnet_18/">18</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">640x320x3</td>
            <td align="right">15.34</td>
            <td align="right">0.588</td>
            <td align="right">0.586</td>
            <td align="center">INT8 </td>
            <td align="right">11.25</td>
            <td align="right">23</td>
            <td align="center" rowspan="2" class="variant"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.resnet18.html#torchvision.models.resnet18">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">960x520x3</td>
            <td align="right">36.01</td>
            <td align="right">0.610</td>
            <td align="right">0.605</td>
            <td align="center">INT8 </td>
            <td align="right">11.25</td>
            <td align="right">64</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="variant"><a href="ResNet/resnet_34/">34</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">7.92</td>
            <td align="right">0.677</td>
            <td align="right">0.588</td>
            <td align="center">INT8 </td>
            <td align="right">21.40</td>
            <td align="right">24</td>
            <td align="center" rowspan="1" class="variant"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.resnet34.html#torchvision.models.resnet34">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center" rowspan="3" class="variant"><a href="ResNet/resnet_50/">50</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">9.09</td>
            <td align="right">0.719</td>
            <td align="right">0.716</td>
            <td align="center">INT8 </td>
            <td align="right">25.10</td>
            <td align="right">30</td>
            <td align="center" rowspan="3" class="variant"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.resnet50.html#torchvision.models.resnet50">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">640x320x3</td>
            <td align="right">29.95</td>
            <td align="right">0.620</td>
            <td align="right">0.619</td>
            <td align="center">INT8 </td>
            <td align="right">24.51</td>
            <td align="right">87</td>
        </tr>
        <tr>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">960x520x3</td>
            <td align="right">77.52</td>
            <td align="right">0.654</td>
            <td align="right">0.650</td>
            <td align="center">INT8 </td>
            <td align="right">24.51</td>
            <td align="right">273</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="variant"><a href="ResNet/resnet_50_v2/">50-v2</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">9.84</td>
            <td align="right">0.697</td>
            <td align="right">0.677</td>
            <td align="center">INT8 </td>
            <td align="right">25.30</td>
            <td align="right">32</td>
            <td align="center" rowspan="1" class="variant"><a href="https://github.com/onnx/models/tree/main/validated/vision/classification/resnet">Github</a></td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="variant"><a href="ResNet/resnet_101/">101</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">14.22</td>
            <td align="right">0.799</td>
            <td align="right">0.618</td>
            <td align="center">INT8 </td>
            <td align="right">43.70</td>
            <td align="right">49</td>
            <td align="center" rowspan="1" class="variant"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.resnet101.html#torchvision.models.resnet101">PyTorch</a></td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="variant"><a href="ResNet/resnet_152/">152</a></td>
            <td align="center">PyTorch</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">18.77</td>
            <td align="right">0.807</td>
            <td align="right">0.586</td>
            <td align="center">INT8 </td>
            <td align="right">59.02</td>
            <td align="right">67</td>
            <td align="center" rowspan="1" class="variant"><a href="https://docs.pytorch.org/vision/main/models/generated/torchvision.models.resnet152.html#torchvision.models.resnet152">PyTorch</a></td>
        </tr>
    </tbody>
</table>

- - -

### Footnote
* PyTorch* models are converted to ONNX for deployment.

