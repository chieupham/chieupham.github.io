---
layout: post
comments: true
title:  "Study industrial cameras"
excerpt: "(Linux)"
date:   2018-07-25 10:00:00
mathjax: false
---

3/
https://www.grainger.com/content/supplylink-video-surveillance-pros-and-cons
https://www.1stvision.com/machine-vision-solutions/2018/03/machine-vision-industrial-camera.html
Advantage: do not depend on other data sets which may have copyright, gather many images of desired objects, provide real-time data, flexibility, working 24/7.

Drawbacks: image quality depends on the cameras (e.g. sensors, technology) and on the condition of scenes, overload data, could be hacked, privacy issue, require multiple accessories, cost of cameras.

4/
https://developers.google.com/machine-learning/crash-course/classification/accuracy
This is a binary classification. To evaluate the performance of this model, we need many metrics. Accuracy is not enough for evaluating because it is sensitive to a class-imbalanced data set. Anna should use other metrics such as Precision and Recall


5/
It is difficult to say what I would do because first of all, I must understand the problematic of our client's projects. It takes a long time to understand these tasks and then plan steps (e.g. finding issue, discussion, proposition of solutions, requesting resources, evaluating solutions, and selection). And perhaps, it takes time to approve a project involve according to the levels (agreements). One day is too hard to finish a job. And one model is not enough to solve a problem.

Assuming that I face a day like your scenario, when I meet our client, I must discuss with him/her to understand their problems. Depending on their tasks, I propose some possible classification methods (maybe trained models with our image acquisition system before the day and some fine-tuning techniques). Then, I evaluate these methods with our servers based on the objective. After that, if one of these models gets results, I deliver to our client. If I cannot finish my job until the end of the day, I will take note issues, get the feedback of clients and recommend another day to accomplish. In the following days, I will discuss with my team, find the solutions and fix the bugs. Then, I continue to come to the client's site on the date of appointment and apply my solutions. Hopefully, it will be accomplished because nothing is perfect. If not, I must repeat other days.

6/
2/10 samples cannot provide exactly the effectiveness of the system. We need more samples to evaluate our model. Assuming that our system committed to a range of the error rate per a number of samples described in the contract with our client. After testing more samples, if the error is in the acceptable range, we will show inspectors that our system still works normally. In the case of higher error, our system has problems and we should be responsible. Immediately, we need to replace current cameras with the new ones. After that, we will look for bugs from the history and the installation of cameras in order to improve our products in the future.

7/
Camera is a real-time device. Assuming that we have a set of cameras through all the conveyor belt. If a strange object falls off on the conveyor, our cameras must detect it and stop the belt. In a simple case, we train our cameras that if an object, which does "not enter the belt at the beginning (at time t=0) or pass through the intermediate positions (e.g. at time t=T, 2T, ...)", is undefined and then a warning will be shown to stop the belt and maybe the operator will take his glasses back.

8/
Nothing is perfect. Even, deep learning is also attacked by adversarial samples. For simplicity, I assume that our train model works in our conditions. When we test them in another place, the quality of captured images may be reduced because of many factors (e.g. light, distances between cameras and objects, undefined objects, the speed of the conveyor belt, accessories, even humidity)

9/
I read StarGAN: Unified Generative Adversarial Networks for Multi-Domain Image-to-Image Translation (CVPR2018) and Progressive Growing of GANs for Improved Quality, Stability, and Variation (ICLR2018). My favorite paper is StarGAN. Actually, I focus on generative adversarial networks (GANs) for unpaired MRI cross-modal synthesis. This paper proposes a method for translating multiple domains within single GANs by mask vectors and a conditioned discriminator. I develop 3D StarGANs for my task, but the results have a lot of artifacts. Fortunately, the technique of neural style transfer, which I studied before, helps me improve 3D StarGANs for solving my problem.

10/
I am fluent in Python, Matlab and C++. I think that I like Python most because it is simple, common and high-level. Almost deep learning frameworks support Python. There are a lot of Python libraries on the internet where I can find by just a click. With the support of Anaconda, I can download the desired libraries. However, Python has disadvantages about speed and embedded systems

11/
Scikit, Caffe, Theano, Keras, Tensorflow, Pytorch. With simple machine learning methods, I use Scikit. There are a lot of methods and examples in the site of Scikit. However, Scikit does not now support GPU training for deep learning. Previously, I used Caffe, one of the first frameworks of deep learning, for training my models. Caffe is free, simple and built-in. However, it has some disadvantages dealing with large size images and writing my own layers. So, in order to test trained models, I had to import the parameters into Lasagne (a lightweight library in Theano) for testing. Another drawback of Caffe is that it does not support shared weight training, which is necessary for training generative adversarial networks. Therefore, Caffe2 is built (but I do not use Caffe2). In addition, Theano is no longer supported. Before Keras, I have tried Tensorflow, but I had problems with the weight storage and it is so messy, despite Tensorflow has almost tools for machine learning and deep learning. And then I found my solution when I started working with Keras. Actually, I use Keras (Tensorflow backend) for training my networks. Keras is free, lightweight and easy to use. In order to writing my own layers, I can exploit Tensorflow backend. Keras helps me to code what I need now. I have coded Pytorch one time, it's also easy to use, but now Keras with Tensorflow backend is enough for my current tasks.

12/
For simplicity, an optimization method such as stochastic gradient descent consists of two steps: forward and backward. The forward pass computes the output of the given input from the first to the last layer and the error between this output and the given output by a loss function. The backward pass computes the gradient of the loss, the gradient of each layer from the loss to the first layer and the whole model. This is called back-propagation.

13/ 
Given a training dataset which consists of  pairs of input and corresponding output, and a predefined architecture of a network, network parameters are estimated by minimizing an objective function using optimization algorithms. Here, we use a mini-batch stochastic gradient descent with momentum (SGD). SGD proposes to update the network parameters $\theta$ at iteration $t+1$ using the negative gradient of the objective function $\nabla \mathcal{L}(\theta_t)$ at iteration $t$, described as: $V_{t+1}= \mu V_t - \alpha\nabla \mathcal{L}(\theta_t) $ and $\theta_{t+1}=\theta_t+V_{t+1}$. where $V_t$ denotes the weight update, $\mu$ and $\alpha$ are respectively the momentum and learning rate.
