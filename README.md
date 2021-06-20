# Currency denomination identification using MASK-RCNN 
Sample project for instance segmentation. Here users can upload an image and test the implementation of instance segmentation. The project can be used for currency denomination identification. Denominations used are from the Indian currency system were in use till August 2019.

### Flow used in project preparation:

1. Prepared Images related to Indian currency denomination with total of 1000 Images of different denomination (100 each).
2. Preparing image annotation using VGG Image annotator[[VGG](https://www.robots.ox.ac.uk/~vgg/software/via/)] with total data set containing 1500 images.
3. Splitting images in train (1100, 100 for each denomination and 100 for mixed denomination class), validation (250) and test (250).
4. It took 2-3 minutes per image for the annotation of a single class in it. With multiple classes it took 5 minutes per image.
5. Preparing model with Mask-RCNN, using transfer learning approach (for this with COCO model generated by [waspinator](https://github.com/waspinator/deep-learning-explorer/tree/master/data)) and checking results.
6. Flask bootstrap for sample HTML page for input and output of the response.
7. Using Google text to speech ([GTTS](https://gtts.readthedocs.io/en/latest/)) for getting results in audio format.

Use case for this web based approach can be. If it is used as an application for detecting number of images and identiyfing each with audio as output, then it can be used for visually impaired persons. Here the approach used is from web-cam, input from other cams can also be considered.

For detailed understanding check [Document_for_understanding](https://github.com/TejasBajania/Mtech_pro/blob/master/Document_for_understanding.pdf).

## Blog referred
https://patrickwasp.com/train-a-mask-r-cnn-model-on-your-own-dataset/

## Models used for implementing

- Mask R-CNN (object detection and segmentation) [[arXiv](https://arxiv.org/abs/1703.06870), [source](https://github.com/matterport/Mask_RCNN)]
- FCN (class segmentation) [[arXiv](https://arxiv.org/abs/1605.06211), [source](https://github.com/aurora95/Keras-FCN)]

## Example input of Image with single denomination
![single_class](https://user-images.githubusercontent.com/33371855/122665007-5bdcf500-d1c2-11eb-9517-5914649c10af.jpg)

## Output generated by model with single denomination

![normal_detect_single](https://user-images.githubusercontent.com/33371855/122665168-4fa56780-d1c3-11eb-9d86-0706731527c5.JPG)

## Example input of Image with dense Indian currencies

![Test_image (9)](https://user-images.githubusercontent.com/33371855/122665254-cd697300-d1c3-11eb-8363-72c9fc3dab91.jpg)

## Output generated by model with dense Indian currencies

![normal_detect1](https://user-images.githubusercontent.com/33371855/122665323-2df8b000-d1c4-11eb-8916-223d4ba5328b.JPG)

<strong>Model detected multiple denomination in an image with average precision (MAP) of 80. </strong>


