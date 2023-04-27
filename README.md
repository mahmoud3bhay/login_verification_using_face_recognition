# login_verification_using_face_recognition

To create a complete project on Face Recognition, we must work on 3 very distinct phases:

-Face Detection and Data Gathering
-Train the Recognizer
-Face Recognition

Face Detection
The most basic task on Face Recognition is of course, “Face Detecting”. Before anything, you must “capture” a face (Phase 1) in order to recognize it, when compared with a new face captured on future (Phase 3).

The most common way to detect a face (or any objects), is using the “Haar Cascade classifier”

Object Detection using Haar feature-based cascade classifiers is an effective object detection method proposed by Paul Viola and Michael Jones in their paper, “Rapid Object Detection using a Boosted Cascade of Simple Features” in 2001. It is a machine learning based approach where a cascade function is trained from a lot of positive and negative images. It is then used to detect objects in other images.


Data Gathering 
we will simply create a dataset, where we will store for each id, a group of photos in gray with the portion that was used for face detecting.
I am capturing few samples from each id.

trainer 
On this phase, we must take all user data from our dataset and “trainer” the OpenCV Recognizer. This is done directly by a specific OpenCV function. The result will be a .yml file that will be saved on a “trainer/” directory.


Recognizer
 Here, we will capture a fresh face on our camera and if this person had his face captured and trained before, our recognizer will make a “prediction” returning its id and an index, shown how confident the recognizer is with this match.
