# Face recognition
  Face recognition using triplet loss, implementing FaceNet with pytorch. A small face dataset which consists of 62 IDs with 20 face images per ID for testing. The algorithm achieves accuracy aboe 95%.
</br>
  人脸识别项目，提供一个小型数据集用作验证，使用三元组损失函数提升准确率和泛化能力，对FaceNet进行了一种实现。提供了一个小型的人脸数据集用于测试和验证。总共62个人，每人20张人脸图像。
</br> </br>

## Dependencies(依赖模块)
    python3, pytorch, torchvision, opencv-python, numpy, tqdm. etc.
## Module components(模块组成)
### dataset module taking care of triplet selection and data loding.(数据集模块主要负责三元组选择和数据加载)
    dataset.py
### utility module taking care of image data formating, cleaning, and organization.（工具模块负责人脸数据的格式转换，数据清洗和数据组织）
    utils.py
### main module in charge of model definition, data/checkpoint loading, training, testing and validation.(主功能模块负责模型定义，数据、断点加载，训练，测试和验证。)
    main.py
## 脚本运行效果截图：
![](https://github.com/CaptainEven/Face-recognition-/blob/master/train.png)
</br>

## Algorithm description(算法说明)
  Inspired by Google's FaceNet, we design a special loss to improve the model's descriminative power for fine-grained classification task   like face recognition. The basic principle is quite plain and simple: if a group face images belong to one person identity, they are definitelt closer to each other than image faces belonging to other person's identity. Its main thought is similar to clusting algorithm.
</br>
  受谷歌FaceNet的启发，我们设计了一种特殊的损失函数(类似于三元组损失函数)，用来提升细粒度分类任务的性能，比如人脸识别任务。它的基本思想简单而朴素，如果一组人脸图像属于同一个人，那么这些图像相比其他人的人脸图像，他们之间肯定会更近似彼此。这个思想类似于聚类。
