# Assignment-2.5

# DataSet Creation

Take Fashion MNIST images and and for each image create 10 tuples for training data and training labels.
e.g: if image is 5 
training_data(sample)    labels
(image,0)                (5, 5+0)
(image,1)                (5, 5+1)
(image,2)                (5, 5+2)
(image,3)                (5, 8)
(image,4)                (5, 9)
(image,5)                (5, 10)
(image,6)                (5, 11)
(image,7)                (5, 12)
(image,8)                (5, 13)
(image,9)                (5, 14)

Similar way for all images for creating training data. Input of model will be training _data containing two inputs(image, random_number)
and will output two things(image prediction no and sum with random number)

# Use in Model

Model will accept two inputs: image and random number
On image, apply normal convolution, relu and fully connected layer to produce output of 60 dimensions.
For random number., one hot encode it to 10 dimensions.
Then combine above two to form 70 dimensions and apply fully connected layer to convert it to 10 no outputs.
Then apply softmax on this output and return that
For another output , predict the image no by argmax softmax and then return addition with random number

Loss = cross_entropy loss between only image prediction and true label. Not considering sum term in loss.
num correct is also as per correct image predictions.

# Training Log:

![image](https://user-images.githubusercontent.com/109232157/211129287-d5151730-73af-4594-ba3d-eb9848c283e3.png)
