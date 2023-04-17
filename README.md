# Welcome!
This repo uses official implementations (with modifications) of [YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://github.com/WongKinYiu/yolov7) and [Simple Online and Realtime Tracking with a Deep Association Metric (Deep SORT)](https://github.com/nwojke/deep_sort)  to detect objects from images, videos and then track objects in Videos (tracking in images does not make sense)

I have refactored the code, removed dependencies, removed extra code so that you can use **ANY** detector model with `DeepSORT`. Please look at the `Demo.ipynb` notebook on how to use the code.

![yolov7_gif](https://user-images.githubusercontent.com/50293852/179401908-bb40a5aa-1209-4efd-924a-641300bb456a.gif)


# Steps:
To use in `Colab`: Open `Colab Demo.ipynb`

For use in local system, please follow the below steps

1. Clone the repo as `git clone https://github.com/deshwalmahesh/yolov7-deepsort-tracking/`
2. Download the weights of any of the pre trained `YOLOv7` models from the links: [`yolov7.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt) [`yolov7x.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7x.pt) [`yolov7-w6.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-w6.pt) [`yolov7-e6.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-e6.pt) [`yolov7-d6.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-d6.pt) [`yolov7-e6e.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-e6e.pt)
3. **NOTE**: Every model has it's own  parameters like `image_size` and all so you have to use the appropriate parameters. This repo was tested successfully with [`yolov7x.pt`](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7x.pt)
4. Go to `Demo.ipynb` and run the code. 

# Troubleshooting
This code works **perfectly** with `python== 3.7, tensorflow==2.8.0, torch== 1.8.0, sklearn==0.24.2` on local **Ubuntu: CPU** as well as **Colab: CPU + GPU** as of `13/07/2022`.


One of the most frequent problem is with the `PATH` such as model weights, input, output etc so pass in the path of the weights carefully. Do not just `run all` all the cells given in the notebook. this code works perfectly as long as you pass the correct path.



