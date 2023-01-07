# Audio-MNIST-Digit-Recognition
This is an exploratory jupyter notebook in the creation and tuning of audio models using Artificial Neural Networks.

## Objective
Build an Artificial Neural Network that can examine the spectrograms of recorded audio of spoken digits and classify them into 10 classes each of which are representative of 10 digits 0 through 9. Then, tune the model to identify architecture vs. resource requirements with respect to number of layers and number of epochs.

## [Dataset](https://www.kaggle.com/datasets/alanchn31/free-spoken-digits)
The dataset comes from the Audio MNIST dataset.

## Observations & Summary
- Given a single input and output, the model still performs with an accuracy of 99% with only approximately 5,000 parameters.
- This is a quarter of the original number of parameters while maintaining the same performance.
- The accuracy of the first epoch was 0.3683 whereas the accuracy of the original model on the first epoch was higher: .4171.
- The original model size was 164 kb in total with 25,000 parameters. With only 5000 parameters and 156 kb, the model is 4.0878% smaller on device.
- The change in accuracy indicates that the model is a different architecture as the number of hidden layers is decreased yet the accuracy remains consistent at 99%.
- The model loss stabilizes around 5 epochs, and the accuracy vs validation accuracy becomes stable at approximately 15 epochs. With the model being trained under 100 epochs, it is clear that less resources are required to accurately train this model.
