<h2>TensorFlow-FlexUNet-Image-Segmentation-Lumbar-Spine (2026/02/26)</h2>
Sarah T.  Arai<br>
Software Laboratory antillia.com<br><br>
This is the first experiment of Image Segmentation for <b>Lumbar-Spine</b> based on our <a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet</a> 
(TensorFlow Flexible UNet Image Segmentation Model for Multiclass), 
and a PNG 
<a href="https://drive.google.com/file/d/10cmxgFT1Y8r7aYRt6WnaJbsWawr7OOmB/view?usp=sharing">
<b>Lumbar-Spine-ImageMask-Dataset.zip</b></a> with colorized masks which was derived by us from <br><br>
<a href="https://www.kaggle.com/datasets/dankok/spider-lumbar-spine-segmentation-in-mr-images">
<b>Lumbar Spine - [Segmentation]</b> </a> on the kaggle.com.
<br><br>
<hr>
<b>Actual Image Segmentation for Lumbar-Spine Images </b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to the ground truth masks.
<br>
<a href="#color-class-mapping-table">Color class mapping table</a>
<br><br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10008_12.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10008_12.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10008_12.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10015_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10015_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10015_3.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10030_2.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10030_2.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10030_2.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1  Dataset Citation</h3>
The dataset used here was derived from <br><br>
<a href="https://www.kaggle.com/datasets/dankok/spider-lumbar-spine-segmentation-in-mr-images">
<b>Lumbar Spine - [Segmentation]</b> </a> <br>
<b>SPIDER - Lumbar spine segmentation in MR images</b> 
on the kaggle.com.
<br><br>
The following explanation was taken from the kaggle web site.
<br><br>
<b>About Dataset</b><br>
This is a large publicly available multi-center <b>lumbar spine magnetic resonance imaging (MRI)</b> dataset with reference segmentations 
of <b>vertebrae, intervertebral discs (IVDs), and the spinal canal.</b>
<br>
The dataset includes <b>447 sagittal T1 and T2 MRI series</b> from <b>218 studies of 218 patients</b> with a history of low back pain.<br>
The data was collected from <b>four different hospitals</b>.<br>
There is an additional hidden test set (not available here) used in the accompanying <b>SPIDER challenge</b> on spider.grand-challenge.org.
<br><br>
<b>Dataset Details</b><br>
The assignment of MRI studies to training and validation sets can be found in the overview file. This file also provides:<br>
<ul>
<li>The biological sex of all patients</li>
<li>The age of patients (where available)</li>
<li>A number of scanner and acquisition parameters for each MRI study</li>
</ul>
<br>
The dataset also comes with radiological gradings (in a separate file) for the following degenerative changes:
<br>
1. Modic changes (type I, II, or III)<br>
2. Upper and lower endplate changes / Schmorl nodes (binary)<br>
3. Spondylolisthesis (binary)<br>
4. Disc herniation (binary)<br>
5. Disc narrowing (binary)<br>
6. Disc bulging (binary)<br>
7. Pfirrman grade (grade 1 to 5)<br>
All radiological gradings are provided per IVD level.
<br><br>
Dataset and public benchmark described in the paper:
<a href="https://www.nature.com/articles/s41597-024-03090-w">
<b>Lumbar spine segmentation in MR images: a dataset and a public benchmark</b></a>
<br>
Public segmentation challenge:<a href="https://spider.grand-challenge.org/"><b>SPIDER Challenge</b></a><br>
<br>
<b>License</b><br>
<a href="https://creativecommons.org/licenses/by/4.0/">Attribution 4.0 International (CC BY 4.0)</a>
<br>
<br>
<h3>
2 Lumbar-Spine ImageMask Dataset
</h3>
 If you would like to train this Lumbar-Spine Segmentation model by yourself,
please down load our dataset <a href="https://drive.google.com/file/d/10cmxgFT1Y8r7aYRt6WnaJbsWawr7OOmB/view?usp=sharing">
<b>Lumbar-Spine-ImageMask-Dataset.zip</b>
</a> on the google drive, expand the downloaded, and put it under <b>./dataset/</b> to be.
<pre>
./dataset
└─Lumbar-Spine
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
        ├─images
        └─masks
</pre>
We used the following 10 classes and colors mapping table to generate the <b>Lumbar-Spine-ImageMask-Dataset</b> with colorized masks from
the <b>SPIDER</b> MHA images and masks dataset.
<br><br>
<a id="color-class-mapping-table"><b>Lumbar-Spine color class mapping table</b></a>
<br>
<table border=1 style='border-collapse:collapse;' cellpadding='5'>
<tr><th>Indexed Color</th><th>Color</th><th>RGB</th><th>Class</th></tr>
<tr><td>0</td><td with='80' height='auto'><img src='./color_class_mapping/Class_0.png' widith='40' height='25'></td><td>(0, 0, 0)</td><td>Class_0</td></tr>
<tr><td>1</td><td with='80' height='auto'><img src='./color_class_mapping/Class_1.png' widith='40' height='25'></td><td>(255, 0, 0)</td><td>Class_1</td></tr>
<tr><td>2</td><td with='80' height='auto'><img src='./color_class_mapping/Class_2.png' widith='40' height='25'></td><td>(0, 255, 0)</td><td>Class_2</td></tr>
<tr><td>3</td><td with='80' height='auto'><img src='./color_class_mapping/Class_3.png' widith='40' height='25'></td><td>(0, 0, 255)</td><td>Class_3</td></tr>
<tr><td>4</td><td with='80' height='auto'><img src='./color_class_mapping/Class_4.png' widith='40' height='25'></td><td>(255, 255, 0)</td><td>Class_4</td></tr>
<tr><td>5</td><td with='80' height='auto'><img src='./color_class_mapping/Class_5.png' widith='40' height='25'></td><td>(255, 0, 255)</td><td>Class_5</td></tr>
<tr><td>6</td><td with='80' height='auto'><img src='./color_class_mapping/Class_6.png' widith='40' height='25'></td><td>(0, 255, 255)</td><td>Class_6</td></tr>
<tr><td>7</td><td with='80' height='auto'><img src='./color_class_mapping/Class_7.png' widith='40' height='25'></td><td>(128, 128, 128)</td><td>Class_7</td></tr>
<tr><td>8</td><td with='80' height='auto'><img src='./color_class_mapping/Class_8.png' widith='40' height='25'></td><td>(255, 255, 255)</td><td>Class_8</td></tr>
<tr><td>9</td><td with='80' height='auto'><img src='./color_class_mapping/Class_9.png' widith='40' height='25'></td><td>(128, 80, 0)</td><td>Class_9</td></tr>
</table>
<br><br>
<b>Lumbar-Spine Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/Lumbar-Spine/Lumbar-Spine_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images of train and valid datasets is large enough to use for a training set of our segmentation model.
<br><br>

<b>Train_images_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_masks_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/train_masks_sample.png" width="1024" height="auto">
<br>
<h3>
3 Train TensorflowFlexUNet Model
</h3>
 We trained Lumbar-Spine TensorflowFlexUNet Model by using the following
<a href="./projects/TensorFlowFlexUNet/Lumbar-Spine/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/Lumbar-Spine, and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
, which simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>
<b>Model parameters</b><br>
Defined a small <b>base_filters=16</b> and a large <b>base_kernels=(11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large num_layers (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
image_width    = 512
image_height   = 512
image_channels = 3
input_normalize = True
normalization  = False
num_classes    = 10
base_filters   = 16
base_kernels  = (11,11)
num_layers    = 8
dropout_rate   = 0.05
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and "dice_coef_multiclass".<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b >Learning rate reducer callback</b><br>
Enabled learing_rate_reducer callback, and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.5
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with patience parameter.
<pre>
[train]
patience      = 10
</pre>
<b></b><br>
<b>RGB color map</b><br>
rgb color map dict for Lumbar-Spine 1+9 classes.<br>
<pre>
[mask]
mask_file_format = ".png"
;Lumbar-Spine 1+9
rgb_map = {(0,0,0):0, (255,0,0):1,(0,255,0):2,(0,0,255):3, (255,255,0):4,(255,0,255):5, (0,255,255):6,(128,128,128):7,(255,255,255):8, (128,80,0):9}
</pre>
<b>Epoch change inference callbacks</b><br>
Enabled epoch_change_infer callback.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
epoch_changeinfer        = False
epoch_changeinfer_dir    = "./epoch_changeinfer"
num_infer_images         = 6
</pre>
By using this epoch_change_infer callback, on every epoch_change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> <br> 
<b>Epoch_change_inference output at starting (1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middle-point (8,9,10)</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/epoch_change_infer_at_middlepoint.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at ending (18,19,20)</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>

<br>
In this experiment, the training process was terminated at epoch 20.<br><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/train_console_output_at_epoch20.png" width="880" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/Lumbar-Spine/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/Lumbar-Spine/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>
4 Evaluation
</h3>
Please move to a <b>./projects/TensorFlowFlexUNet/Lumbar-Spine</b> folder, and run the following bat file to evaluate TensorflowFlexUNet model for Lumbar-Spine.<br>
<pre>
>./2.evaluate.bat
</pre>
This bat file simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetEvaluator.py  ./train_eval_infer.config
</pre>
Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/evaluate_console_output_at_epoch20.png" width="880" height="auto">
<br><br>Image-Segmentation-Lumbar-Spine

<a href="./projects/TensorFlowFlexUNet/Lumbar-Spine/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to this Lumbar-Spine/test was low, and dice_coef_multiclass high as shown below.
<br>
<pre>
categorical_crossentropy,0.0159
dice_coef_multiclass,0.9917
</pre>
<br>
<h3>5 Inference</h3>
Please move to a <b>./projects/TensorFlowFlexUNet/Lumbar-Spine</b> folder, and run the following bat file to infer segmentation regions for images by the Trained-TensorflowFlexUNet model for Lumbar-Spine.<br>
<pre>
>./3.infer.bat
</pre>
This simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/mini_test_masks.png" width="1024" height="auto"><br>
<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks for  Lumbar-Spine  Images</b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to the ground truth masks.
<br>
<a href="#color-class-mapping-table">Color class mapping table</a>
<br>
<br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10009_4.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10009_4.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10009_4.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10009_13.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10009_13.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10009_13.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10010_6.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10010_6.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10010_6.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10019_10.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10019_10.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10019_10.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10028_13.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10028_13.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10028_13.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/images/10029_10.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test/masks/10029_10.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Lumbar-Spine/mini_test_output/10029_10.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>

<b>1. Lumbar spine segmentation in MR images: a dataset and a public benchmark</b><br>
Jasper W. van der Graaf, Miranda L. van Hooff, Constantinus F. M. Buckens, Matthieu Rutten, Job L. C. van Susante, <br>
Robert Jan Kroeze, Marinus de Kleuver, Bram van Ginneken & Nikolas Lessmann<br>
<a href="https://www.nature.com/articles/s41597-024-03090-w">
https://www.nature.com/articles/s41597-024-03090-w</a>
<br>
<br>
<b>2. Lumbar spine segmentation method based on deep learning</b><br>
Hongjiang Lu, Mingying Li, Kun Yu, Yingjiao Zhang, Liang Yu<br>
<a href="https://aapm.onlinelibrary.wiley.com/doi/10.1002/acm2.13996">
https://aapm.onlinelibrary.wiley.com/doi/10.1002/acm2.13996</a>
<br><br>
<b>3. Automatic semantic segmentation of the lumbar spine: Clinical applicability in a multi-parametric and multi-center study on magnetic resonance images</b><br>
Jhon Jairo Sáenz-Gamboa, Julio Domenech, Antonio Alonso-Manjarrés, Jon A. Gómez, Maria de la Iglesia-Vayá <br>
<a href="https://www.sciencedirect.com/science/article/pii/S0933365723000738">
https://www.sciencedirect.com/science/article/pii/S0933365723000738</a>
<br><br>
<b>4. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai <br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model
</a>
<br>
<br>
