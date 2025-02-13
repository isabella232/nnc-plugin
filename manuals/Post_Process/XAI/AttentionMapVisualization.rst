XAI/Attention Map Visualization
~~~~~~~~~~~~~~~~~~~~~

Using the method called Attention Branch Network, the areas of the input image that affect the classification result are made visible in the model, which performs image classification.

| Attention Branch Network:
| `Hiroshi Fukui, Tsubasa Hirakawa, Takayoshi Yamashita, Hironobu Fujiyoshi. "Attention Branch Network: Learning of Attention Mechanism for Visual Explanation". 2019 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR). <https://ieeexplore.ieee.org/document/8953929>`_

Input Information
===================

.. list-table::
   :widths: 30 70
   :class: longtable

   * - model
     -
        Specify the model file (*.nnp) that will be used in the Attention Map Visualization computation.
        
        To perform Attention Map Visualization based on the training result selected in the Evaluation tab, use the default results.nnp.

   * - image
     -
        Specify the image file to analyze.
        
        To perform Attention Map Visualization on a specific image shown in the evaluation results of the Evaluation tab, start the plugin with the cell containing the image file name selected. The image file name will be automatically input in image.

   * - output
     -
        Specify the name of the image file to output the visualization results to.
        
        If Attention Map Visualization is executed from the evaluation results of the Evaluation tab, the visualization results are saved to the specified file in the training result folder.

   * - attention_map_layer
     - For SHAP processing, specify the layer of interest for which SHAP computation is executed. Designate the layer counts from the input layer (input is counted as 0th layer). By default, it is processed with input layer.

Output Information
===================

The result of this plugin is saved in the designated 'output' path as PNG file.
It is shown in jet colormap over the original image, where reddish color means the positively affected area.
