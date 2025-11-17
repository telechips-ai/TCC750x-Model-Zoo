# FlowNet Series Benchmark on TCC750x

The following table shows benchmark results for FlowNet optical flow models running on the TCC750x NPU.
You can compare the performance of each model.

FlowNet predicts dense 2D motion (optical flow) between two images in a single forward pass and is widely used as a baseline for learning-based flow estimation.

Click on the model name to download a tar file containing the model binary for TCC750x.

**Note**: FlowNetPytorch is a PyTorch implementation of FlowNet by Dosovitskiy et al. (see references).

- - -

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model     |
| **Framework**            | Deep learning framework used (e.g., PyTorch\*, TFLite, ONNX)                 |
| **Dataset**              | Dataset used to benchmark model performance (e.g., FlyingChairs)                               |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC750x EVB using zero-padded input images                               |
| **EPE**             | Endpoint Error (EPE) is evaluated on the FlyingChairs dataset (22,872 image pairs)                |
| **F1-all (%)**             | The percentage of outliers averaged over all pixels, where outliers are defined as EPE > 3 pixels or > 5%.                  |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: Weight and Bias Binary (.bin) and Command Binary (.bin) for execution on TCC750x    |
| **References**           | Link and license\** information for the original repository of the model       |



---
<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Framework</th>
            <th rowspan="2">Dataset</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th colspan="2">EPE</th>
            <th colspan="2">Fl-all (%)</th>
            <th rowspan="2">Quantization Bit</th>
            <th colspan="2">Compiled Model Files</th>
            <th colspan="2">References</th>
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
                <td align="center" rowspan="2" class="model"><a href="#">FlowNetS</a></td>
                <td align="center" class="variant" rowspan="1"><a href="flownets/">-</a></td> <!-- Models: Variant -->
                <td align="center">PyTorch</td> <!-- Framework -->
                <td align="center">FlyingChairs</td>
                <td align="center">512x384x3 (1 pair)</td> <!-- Input Size (WxHxC) -->
                <td align="right">29.8</td> <!-- Inference Time (msec): EVB -->
                <td align="right">1.839</td>
                <td align="right">4.829</td>
                <td align="right">11.02</td>
                <td align="right">29.56</td>
                <td align="center">INT8</td>
                <td align="right">39.1</td>
                <td align="right">104</td>
                <td align="center" rowspan="2"><a href="https://github.com/ClementPinard/FlowNetPytorch?tab=readme-ov-file">GitHub<a></td> <!-- References: Link -->
                <td align="center" rowspan="2">MIT</td>
            </tr>
            <tr>
                <td align="center" class="variant" rowspan="1"><a href="flownets/">BN</a></td> <!-- Models: Variant -->
                <td align="center">PyTorch</td> <!-- Framework -->
                <td align="center">FlyingChairs</td>
                <td align="center">512x384x3 (1 pair)</td> <!-- Input Size (WxHxC) -->
                <td align="right">29.8</td> <!-- Inference Time (msec): EVB -->
                <td align="right">2.442</td>
                <td align="right">5.523</td>
                <td align="right">14.28</td>
                <td align="right">38.28</td>
                <td align="center">INT8</td>
                <td align="right">39.1</td>
                <td align="right">104</td>
            </tr>
        <tbody>
    <tbody>
        <tr>
        </tr>
    </tbody>
</table>

- - -

## 📤 Output Format
- The raw output is a dense optical flow tensor of shape 2×H×W per image pair, where (u, v) represent the horizontal and vertical pixel displacements, respectively.
- Coordinates follow image axes: +u/-u → right/left, +v/-v → down/up.
- Common post-processing:
    - Resize flow back to the original image resolution (scale u and v by width/height ratios).
    - Color visualization with a flow color wheel (hue = direction, value = magnitude) for quick inspection.

### Footnote
* PyTorch* models are converted to ONNX for deployment.

* License\**:
  - Telechips Inc. is not responsible for any issues, damages, or losses resulting from the use of code downloaded from GitHub repositories provided by Telechips.
  - The performance results of neural networks (such as, mAP or inference time) are not subject to license term and may be used freely.
  - Any output generated by software execution may or may not be subject to license terms, depending on the contract and intended use of the output.




