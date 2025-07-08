# LeNet5 Benchmark on TCC750x

The following table shows benchmark results for the LeNet5 model running on the TCC750x NPU.  
LeNet5 is a family of lightweight and efficient convolutional neural networks optimized for image classification tasks, particularly on embedded and mobile devices. 

The LeNet5 model is evaluated using the MNIST validation dataset and compiled with the tc-nn-toolkit toolkit.  
Click on the model name to download a tar file containing the model binary for TCC750x.

---

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model      |
| **Framework**            | Deep learning framework used (e.g., PyTorch\*, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance (e.g., MNIST validation set with 10,000 images)  |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) and dimensions of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC750x EVB using zero-padded input images                |
| **Accuracy**             | Top-1 classification accuracy on the MNIST validation dataset (10,000 images)                    |
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
            <th>Weight and Bias Binary (MB)</th>
            <th>Command Binary (KB)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="2"><a href="lenet5/">LeNet5</a></td>
            <td align="center">PyTorch</td>
            <td align="center">MNIST</td>
            <td align="center">32x32x1</td>
            <td align="center">0.05</td>
            <td align="center">0.986</td>
            <td align="center">0.982</td>
            <td align="center">INT8 </td>
            <td align="center">0.05</td>
            <td align="center">2</td>
            <td align="center"><a href="https://huggingface.co/mindspore-ai/LeNet">Hugging Face</a></td>
        </tr>
    </tbody>
</table>

- - -

## 📤 Output Format

- The model returns the index of the top-1 class with the highest confidence score among  10 MNIST classes representing digits 0 to 9.

- - -

### Footnote                
* PyTorch* models are converted to ONNX for deployment.
