# Aerial-Cactus
Notebook for Aerial Cactus competition on Kaggle.
My take on the Aerial Cactus competition on Kaggle is in the code notebook provided.

I have used Google Colaboratory (because who doesn't want to work with more RAM and better GPU). If you don't want to used Google Colaboratory (your loss), comment out the first four cells in the notebook.


![unbalanced](https://user-images.githubusercontent.com/29707088/58657651-60fd4c00-833c-11e9-8a68-3cb3431da907.png)

First thing I did was to augment the dataset because we have only 17000 images here, which won't give us any satisfactory result with neural nets. So for this I have simply just appended the images in a list and then used numpy filpud, fliplr, rot90 functions to augment the images. And voila, we now have 70,000 images (something to work with).

Now I normalized images between [0,1]. This always helps so that all inputs from images are in comparable range.

Then I applied a simple CNN model giving me an accuracy of 95% on separated test data.
Unsatisfied with my accuracy (too much greed), I tried using VGG16 model. This gave me an accuracy of 97% (better!).

Check out the accuracy and loss plots  below:

![acc-loss plot](https://user-images.githubusercontent.com/29707088/58657479-f77d3d80-833b-11e9-8ffa-a542642b718f.png)

Don't forget to check out the ROC curve too, retty helpful.

![roc plot](https://user-images.githubusercontent.com/29707088/58657522-0fed5800-833c-11e9-9346-292cbec5f754.png)
