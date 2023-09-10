This README describes the installation process of the HAM10000 dataset to the Google Colab development workspace
## Installation Steps
Sign in to you Kaggle Account and go to the Settings option. When you access this page, scroll down and you will see a button "Create New Token". Press this button and in your downloads folder you will see a file named kaggle.json. If you open the file you will see that it contains a username and a key.
Now open Google Colab on your browser and create a new notebook. 
Install the kaggle library using the following command
```sh
!pip install -q kaggle
```
Now run the following block of code.
```
from google.colab import files
files.upload()
```
This will give you the option to upload a file. What you need to do is select the kaggle.json file you downloaded.

The next step involves creating a Kaggle folder using the following command on your notebook:
```sh
! mkdir ~/.kaggle
```
After that, copy the kaggle.json file to the kaggle folder with the following command:
```sh
! cp kaggle.json ~/.kaggle/
```
Change the permissions of your file with the following instruction:
```sh
! chmod 600 ~/.kaggle/kaggle1.json
```
Now run this command to download the HAM10000 dataset from kaggle:
```sh
!kaggle datasets download -d kmader/skin-cancer-mnist-ham10000
```

Unzip the folder downloaded using the following command:
```sh
!unzip skin-cancer-mnist-ham10000.zip
```

The HAM10000 has been imported successfully to your Google colab workspace. All you have to do now is to place the folder inside the project directory and you are ready to go!!!