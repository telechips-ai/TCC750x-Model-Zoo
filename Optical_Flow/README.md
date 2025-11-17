# Optical Flow Benchmark on TCC750x

The following table shows benchmark results for various Optical Flow models running on the TCC750x NPU.
You can compare the performance of each model.

Click on the model name to download a tar file containing the model binary for TCC750x.

---

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
| **Compiled Model Files**   | Sizes of the compiled model components: Weight and Bias Binary (.bin) and Command Binary (.bin) for execution on TCC750x    |****
| **References**           | Link to the original repository of the model                         |



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
            <th colspan="2">F1-all (%)</th>
            <th rowspan="2">Quantization Bit</th>
            <th colspan="2">Compiled Model Files</th>
            <th colspan="1">References</th>
        </tr>
        <tr>
            <th>FP32</th>
            <th>INT8</th>
            <th>FP32</th>
            <th>INT8</th>
            <th>Weight and Bias Binary (MB)</th>
            <th>Command Binary (KB)</th>
            <th>Link</th>
        </tr>
    </thead>
        <tbody>
            <tr>
                <td align="center" rowspan="2" class="model"><a href="FlowNet/flownets/">FlowNetS</a></td>
                <td align="center" class="variant" rowspan="1"><a href="FlowNet/flownets/">-</a></td> <!-- Models: Variant -->
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
            </tr>
            <tr>
                <td align="center" class="variant" rowspan="1"><a href="FlowNet/flownets/">BN</a></td> <!-- Models: Variant -->
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

### Footnote
* PyTorch* models are converted to ONNX for deployment.



