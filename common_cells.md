# Top cell 
import sys
import os
from google.colab import drive

# Change this according to the current section
section_number = 2

#  
drive.mount('/content/gdrive’)

# Setup to use cv.imshow() 
gDrive_location = '/content/gdrive/MyDrive'
module_folder = 'Utilities4Colab'
full_path_module_folder = os.path.join(gDrive_location, module_folder)
sys.path.append(full_path_module_folder)

# Import class and define the instance as cv (therby you can delete only '2' below)
from cv2workaround import Cv2Workaround 
cv = Cv2Workaround()

# file path
project_path = 'Hands-On-Computer-Vision-with-OpenCV-4-Keras-and-TensorFlow-2/'
str_section = 'Section ' + str(section_number)
full_path = os.path.join(gDrive_location, project_path, str_section)
print(full_path)





# Last cell 
drive.flush_and_unmount()
