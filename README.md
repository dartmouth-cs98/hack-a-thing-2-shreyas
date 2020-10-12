# hack-a-thing-2-shreyas

## Short description of what you attempted to build

I wrangled with and worked through tutorials for 3 different technologies/frameworks:

1. [PyTorch](https://github.com/dartmouth-cs98/hack-a-thing-2-shreyas/tree/main/pytorch)
    * A set of simple tutorials to help understand PyTorch’s Tensor library and neural networks at a high level as well as train a small neural network to classify images.
    * [Tutorial here](https://pytorch.org/tutorials/beginner/blitz/tensor_tutorial.html#sphx-glr-beginner-blitz-tensor-tutorial-py)
2. [PySyft](https://github.com/dartmouth-cs98/hack-a-thing-2-shreyas/tree/main/pysyft)
    * Worked through the basics of using PyTorch in PySyft, building a simple deep learning model, advanced tools for pointers to remote data, and anonymous federated learning on remote workers.
    * [Tutorial Here](https://github.com/OpenMined/PySyft/tree/master/examples/tutorials)
3. [Apple HealthKit](https://github.com/shreyas-v-agnihotri/raywenderlich-workout-tracker)
    * Learned how to build an iOS app that uses Apple HealthKit to pull data from and save data to the Health app.
    * [Tutorial Here](https://www.raywenderlich.com/459-healthkit-tutorial-with-swift-getting-started)

The first 2 are contained in Jupyter notebooks in this reposity and the last is located [here on my private github](https://github.com/shreyas-v-agnihotri/raywenderlich-workout-tracker) because of issues integrating 2 independently-managed repositories.

## What you learned

I learned a ton:
* PyTorch: Working with numpy-like matrices in python to represent data that can be analyzed and trained on.
* PySyft: Using an innovative new framework to access data located on remove servers/workers/devices, and integrating model iterations into a single update.
* HealthKit: How to register a barebones iOS app with Apple HealthKit, getting user permission to integrate with their health data, and then using the data from their device to perform computations and push data back to Apple Health.

## How does this hack-a-thing inspire you or relate to your possible project ideas?

PySyft will be the foundation for distributing federated models to developer devices on behalf of our clients. Understanding the mechanics of PyTorch was essential in understanding how data objects work in PySyft, and PySyft itself is likely going to be our framework of choice for interfacing between master models (uploaded by our clients) and worker devices.

Understanding HealthKit is going to be very useful for creating our MVP and POC mobile app that locally holds user data and can allow a model to be trained on it. Health data is a perfect example of otherwise heavily-guarded and privatized data that our clients will want to access and analyze. I feel confident after working through this tutorial that I'll be able to build an iOS app that can hold data from Apple Health, which will be necessary for our Federated Learning process to work end-to-end.

## What didn’t work

It took me some time to understand how PyTorch objects worked, especially the concepts surrounding operations and reshaping. I had the same issue again understanding PySyft pointers, and specifically how operations between pointers translated to changes on remote workers. For the most part, though, these frameworks were easy to pick up and give me confidence about using them as this project moves forward.

There were, as expected, also a ton of technical issues: difficulty installing PyTorch and PySyft using `conda` and `pip`, issues uploading to github due to file limits (the first time I've encountered this issue), and trouble combining 2 different git-tracked repositories (hence why the iOS app is located on my personal repo). These are all learning experiences for the rest of the project as well.
