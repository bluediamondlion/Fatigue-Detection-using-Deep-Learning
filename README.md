<a href="https://doi.org/10.5281/zenodo.3902276"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.3902276.svg" alt="DOI"></a>

# TEST
  This is my first repository and customizing for deep learning project ~~~

# Fatigue Detection using Deep Learning

This repository contains a project based on the research to detect fatigue levels of a person through a photograph. For this project the main facial cues used to detect fatigue levels are: Undereyes, Eyes, Mouth, Nose and Skin.

### Problem Statement
The complexities of fatigue have drawn much attention from researchers across various disciplines. Short-term fatigue may cause safety issue while driving; thus, dynamic systems were designed to track driver fatigue. Longterm fatigue could lead to chronic syndromes, and eventually affect individuals physical and psychological health. Traditional methodologies of evaluating fatigue not only require sophisticated equipment but also consume enormous time.

<p align="center">
<img src="https://user-images.githubusercontent.com/33536225/85205309-42e3fe80-b338-11ea-9966-cf295f576aa3.png" height="200" >
</p>

### Our Proposal
In this project, we attempt to develop a novel and efﬁcient method to predict individual’s fatigue rate by scrutinising human facial cues. Our goal is to predict fatigue rate based on a single photo. Our work represents a promising way to assess sleep-deprived fatigue, and our project will provide a viable and efﬁcient computational framework for user fatigue modelling in large-scale.

### Architecture
The architecture for this project is shown in the picture below. The image of a face is taken as input from which the facial landmarks are detected and cropped out. These cropped out facial landmarks such as eyes, undereyes, nose, mouth along with the entire face image for the skin is fed into individual models trained on these specific features. The individual models return a value which corresponds to the fatigue levels. These values are then taken as a weighted sum (where eyes and undereyes are given more weightage) which is used as the final value to determine the fatigue level of a person.


### Setup Instructions
<ol>
<li>Clone the entire repository into your local machine.</li>
<li>Download contents of <a href="https://zenodo.org/api/files/fc89114d-f49d-42b1-a277-2a2b08bf4ea9/object_detection_folder.zip">object_detection </a> folder from zenodo and place all the contents in the folder.</li>
<li>Download the <a href="https://zenodo.org/api/files/fc89114d-f49d-42b1-a277-2a2b08bf4ea9/image_classification_models.zip"> models </a> from zenodo and place all the contents in models/image_classification.</li>


  <p> Open Anaconda Command Prompt and Setup a new environment</p>
   
  ```
   C:\> conda create -n FatigueDetection pip python=3.6
  ```

  <p>Activate the environment and upgrade pip </p>
  
  ```
  C:\> activate FatigueDetection
  (FatigueDetection) C:\>python -m pip install --upgrade pip
  ```
  <p>All other requirements can be installed using requirements.txt</p>
  
  ```
   (FatigueDetection) C:\>pip install -r requirements.txt
  ```

<li> After all the package installations has been done navigate to the directory where the project has been downloaded and run "config.py":
  
  ```
  (FatigueDetection) C:\> python config.py
  ```
<li> After "config.py" has been run now you can run "app.py":
  
  ```
  (FatigueDetection) C:\> python app.py
  ```
<p align="center"> After running the above command you should get a screen that looks like this.



<li> After running the python script and copying the link to the browser you should get this screen.</li><br>
 
<p> Here you can upload the image using the browse button and selecting the image to check the fatigue levels. Here we have selected an image and are ready to detect the fatigue levels. </p>


<p> After clicking on the predict button this is the result that is found. </p>

<br>


<br>


### Note : The lower the score, the higher level of fatigue.

Current aggregation used for final score:
  ```
(((sum of left eye and right eye scores) / 2)*0.4) + (((sum of left under-eye and right under-eye scores)/2)*0.55) + (((sum of nose, face and mouth scores)/3)*0.05
  ```
This aggregation has been done through basic intuitive hypothesis. Please feel free to assign weights according your own hypothesis. For eg. - Linear Regression can be used to assign specific weights to each part of the face.
<p> Main contributors of the project:

# Extras:

### Credits:
<p> You can follow this <a href="https://github.com/EdjeElectronics/TensorFlow-Object-Detection-API-Tutorial-Train-Multiple-Objects-Windows-10" >link</a> for an excellent tutorial to make train your own custom object detection model. Our under-eye object detection as heavily based on this.</p>
<p> You can follow this <a href="https://www.pyimagesearch.com/2017/04/10/detect-eyes-nose-lips-jaw-dlib-opencv-python/" >link</a> from pyimagesearch for facial part extraction using dlib. Our facial part extraction is heavily based on this.</p>

### Data:
<p> You can download the data used for the project from <a href="https://zenodo.org/api/files/fc89114d-f49d-42b1-a277-2a2b08bf4ea9/dataset.zip">here</a>. </p>



P.S. - If you happen to use any of our code or data for your experiment you can cite our work/data using the zenodo. Just click on the zenodo badge above and you will be redirected to zenodo where you can find how to cite our work.

