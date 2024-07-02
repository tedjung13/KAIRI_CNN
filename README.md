**Introduction**
The given problem is that there are images that need classifying in two ways. First, there is the class, which
talks about the object that is in the image, with 15 different classes. Then, there is also the state, which talks
about the type of anomaly that could be in the image, such as bent-wire, hole, etc. There are 49 different states,
and in total, there are 88 different labels that include both pieces of information for each image. An example
of a label would be “tile-good” or “cable-bent wire.” The first part of the prompt is to distinguish between the
classes, then the second part is to distinguish between “good” and “bad” images.

**Dataset**
The training dataset contains 4,277 images, and the testing dataset contains 2,154 images. All these images
are in folders called train and test respectively, and my idea was to create a new folder that would contain in it
folders corresponding to each label, to pre-distinguish the images from the training set. Looking back, this part
may not be necessary, as we could call the CSV file every time to just read what the label would be, but the
function ImageFolder makes it easy to make a dataset, so I left it. In my code, this would be the train folder,
with folders for every label in it.
One caveat that must be noted is that for this model to run on Google Colab, the folder of testing and training
images must be locally available. The two ways I found was to either upload the folder as a zip file onto Google
Colab directly or download the folder on Google Drive and reference a pathway to it as code. The first option
I estimated to take somewhere between 3-5 days, and the second took about three hours, so that’s what I did.
If there is a better or more time-efficient way to reference the data, please feel free to let me know.
