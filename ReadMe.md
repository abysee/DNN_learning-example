# A simple project for learning CNN on Image classification

### Notice

This project used an example code from Paddle-Paddle's official website which showed how to use Paddle-Paddle's CNN to accomplish an image classification task. I did this as an assignment to learn CNN and had tested its performance on different parameters. For more information of the original code please visit Paddle-Paddle's official website.

### Details



This example used an API provided by Paddle-Paddle for downloading the CIFAR10 dataset and preparing the data iterator for training. The CIFAR10 is composed of 60000 colored pictures with each sized 32*32. Among them 50000 pictures make up the training set and the other 10000 pictures constitute the test set. All the pictures are of 10 classifications and the model is aimed to make the right classification.

Paddle-Paddle defined three 2D-convolution network and used Relu as the active function after each convolution, along with two 2D-Max-pooling layer and two linear layer. This would map a 32*32*3 picture to 10 outputs which corresponding to 10 classifications.

By tuning epoch size bigger the accuracy rate converged a bit faster at the beginning, but the results didn't show much difference between size 15 and 20.

Keeping epoch size as 15 and tuning batch size from 8 to 64, the result showed significant difference that smaller epoch size results in faster convergence rate and vice versa. 

As the learning rate for this model, it performs quite well when it equals 0.001. As I tuned it to 0.0001 its performance has dramatically declined, so I just left it there.



epoch = 10, batch size = 32, learning rate  = 0.001![epoch = 10, batch size = 32, learning rate  = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep10ba32lr10-3.png)

epoch = 15, batch size = 8, learning rate  = 0.001![epoch = 15, batch size = 8, learning rate  = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep15ba8lr10-3.png)

epoch = 15, batch size = 16, learning rate = 0.001![epoch = 15, batch size = 16, learning rate = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep15ba16lr10-3.png)

epoch = 15, batch size = 32, learning rate = 0.001![epoch = 15, batch size = 32, learning rate = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep15ba32lr10-3.png)

epoch = 15, batch size = 32, learning rate = 0.0001![epoch = 15, batch size = 32, learning rate = 0.0001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep15ba32lr10-4.png)

epoch = 15, batch size = 64, learning rate = 0.001![epoch = 15, batch size = 64, learning rate = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep15ba64lr10-3.png)

epoch = 15, batch size = 128, learning rate = 0.001![epoch = 15, batch size = 128, learning rate = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep15ba128lr10-3.png)

epoch = 20, batch size = 32, learning rate = 0.001![epoch = 20, batch size = 32, learning rate = 0.001](https://github.com/abysee/DNN_learning-example/tree/main/result/ep20ba32lr10-3.png)



