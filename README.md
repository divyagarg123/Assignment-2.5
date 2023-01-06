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
total_loss:  2.304561171849569 total_correct:  62922
total_loss:  2.3041157370758056 total_correct:  62722
total_loss:  2.298062359873454 total_correct:  67202
total_loss:  2.2931556158447264 total_correct:  69152
total_loss:  2.2928664020284018 total_correct:  69763
total_loss:  2.302566183827718 total_correct:  62406
total_loss:  2.3113403741200766 total_correct:  59008
total_loss:  2.3077816186269122 total_correct:  59860
total_loss:  2.3069199922943113 total_correct:  60141
total_loss:  2.308131017735799 total_correct:  59625
total_loss:  2.309306469599406 total_correct:  59937
total_loss:  2.3080953948465983 total_correct:  60805
total_loss:  2.3157895592753093 total_correct:  60643
total_loss:  2.3204255466715495 total_correct:  58774
total_loss:  2.317178121210734 total_correct:  56019
total_loss:  2.307277942682902 total_correct:  60593
total_loss:  2.3074359098815918 total_correct:  63477
total_loss:  2.3088055672709147 total_correct:  61244
total_loss:  2.3096833536020913 total_correct:  63407
total_loss:  2.313846346537272 total_correct:  60793
total_loss:  2.308768978093465 total_correct:  61927