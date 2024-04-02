# Video Anaysis


# MODULE 1:Face Recognition Module

## Overview

This module implements a robust face recognition system utilizing advanced computer vision techniques. By harnessing the power of OpenCV, dlib, and collections Python libraries, the system effectively identifies faces in video frames and determines the most frequently occurring face.

## Features

- Seamless extraction of frames from video files stored in Google Drive using OpenCV's VideoCapture class.
- Precise face detection in each frame using dlib's frontal face detector.
- Utilization of the Counter class from the collections module to tally detected faces.
- Determination of the most common face based on the highest count, providing valuable insights into the predominant face in the video dataset.

## Methodology

1. *Video Frame Extraction:*
   - Utilize OpenCV's VideoCapture class to extract frames from a video file stored in Google Drive.
   
2. *Face Detection using Dlib:*
   - Employ dlib library's frontal face detector for accurate face detection in each frame.
   
3. *Face Recognition and Counting:*
   - Leverage the Counter class from the collections module to count occurrences of each detected face.

## Libraries Used

1. *Python:*
   - Primary programming language facilitating scripting and seamless integration.
   
2. *dlib:*
   - Utilized for accurate face detection in every video frame.
   
3. *collections:*
   - Employed to count occurrences of each detected face.
   
4. *OpenCV:*
   - Integral for video frame extraction and proficiently handling image processing tasks.

## Usage

1. Ensure Python and the required libraries are installed.
2. Provide the path to the video file stored in Google Drive.
3. Run the script to extract frames, detect faces, and determine the most common face.


# MODULE 2:Text Detection and Optical Character Recognition (OCR) Module

## Overview

This module focuses on implementing text detection and optical character recognition (OCR) using OpenCV for video processing, Pytesseract for OCR, and the datetime module for timestamp generation. It applies text filtering to remove non-printable characters and meaningless text.

## Methodology

1. *Video Processing:*
   - Open a video file using OpenCV (cv2.VideoCapture()).
   - Iterate through each frame of the video, extracting text using OCR.

2. *Text Extraction:*
   - Utilize Pytesseract library for OCR to extract text from each frame of the video.

3. *Text Filtering:*
   - Apply filtering to remove non-printable characters and meaningless text using the filter_text() function.
   - Remove non-printable characters and filter out single characters or meaningless text.

4. *Timestamp:*
   - Obtain the current timestamp using the datetime.now().strftime() method.
   - Print the timestamp with the date and timestamp in the format hours, minutes, and seconds.

5. *Unique Text Storage:*
   - Utilize a set named unique_text_set to store unique extracted text.

6. *Output:*
   - Print extracted text along with the timestamp to the console.
   - Only unique text is printed due to the presence of the unique_text_set.

## Libraries Used

1. *OpenCV (cv2):*
   - Utilized for video processing, frame extraction, and conversion to grayscale.

2. *Pytesseract:*
   - Employed for Optical Character Recognition (OCR) to extract text from video frames.

3. *Datetime:*
   - Utilized to obtain the current timestamp.

4. *String:*
   - Used for string manipulation, particularly for filtering out non-printable characters.

## Usage

1. Ensure Python and the required libraries are installed.
2. Provide the path to the video file.
3. Run the script to perform text detection and OCR on the video frames.
4. View the extracted text and timestamps in the console output.


#MODULE 3: Image Captioning Module

## Overview

This module implements image captioning, a task involving generating textual descriptions for specific images. The dataset provided for this task was a video, which was converted into individual frames stored in a folder.

## Methodology

1. *Video Processing:*
   - Open a video file using OpenCV (cv2.VideoCapture()).
   - Iterate through each frame of the video, converting each frame to grayscale.

2. *Text Extraction:*
   - Utilize Tesseract OCR (pytesseract.image_to_string()) to extract text from each frame of the video.

3. *Text Cleaning:*
   - Apply regular expressions to clean the extracted text, removing symbols and unwanted characters.

4. *Text Summarization:*
   - Use a pre-trained summarization model for text summarization.
   - Specifically, leverage the BART model, which is a sequence-to-sequence model, for summarization.

5. *Error Handling:*
   - Check if the video file opened successfully and if text was extracted from the video frames.
   - Print appropriate error messages if there are errors in text extraction or if no text is extracted.

## Libraries Used

1. *Python:*
   - Primary programming language for scripting and seamless integration.

2. *pytesseract:*
   - Utilized for Optical Character Recognition (OCR) tasks.

3. *OpenCV:*
   - Can be integrated for additional image processing tasks if required.

4. *re:*
   - The re module is used for text cleaning, specifically to remove symbols from the extracted text.

## Usage

1. Ensure Python and the required libraries are installed.
2. Provide the path to the folder containing the video frames.
3. Run the script to perform image captioning on the video frames.
4. View the generated textual descriptions for the images.


#MODULE 4:Story Generation Module

## Overview

This module generates a narrative story by randomly selecting captions extracted from images and connecting them based on their last words. The primary goal is to create a cohesive narrative story using captions extracted from a video.

## Methodology

1. *Video Processing:*
   - Open the video file using OpenCV (cv2.VideoCapture()).
   - Extract frames iteratively from the video using a loop, converting each frame to grayscale to simplify the OCR process.

2. *Text Extraction:*
   - Employ Pytesseract for Optical Character Recognition (OCR) on the grayscale frames to extract text.

3. *Text Cleaning:*
   - Utilize regular expressions (re) to remove non-alphanumeric characters from the extracted text, aiming to clean the text and remove noise or unwanted symbols.

4. *Text Accumulation:*
   - Accumulate the cleaned text from each frame into a single string, containing all the extracted text from the entire video.

5. *Text Summarization:*
   - Utilize a pre-trained model (facebook/bart-large-cnn) for text summarization to generate a summarized version of the text.

## Libraries Used

1. *OpenCV (cv2):*
   - Utilized for video processing, frame extraction, and conversion to grayscale.

2. *Pytesseract:*
   - Employed for Optical Character Recognition (OCR) to extract text from video frames.

3. *Transformers (pipeline):*
   - Utilized for text summarization using pre-trained Natural Language Processing (NLP) models.

4. *Regular Expressions (re):*
   - Used for text cleaning by removing non-alphanumeric characters.

## Usage

1. Ensure Python and the required libraries are installed.
2. Provide the path to the video file.
3. Run the script to generate a narrative story using captions extracted from the video frames.
4. View the generated narrative story.
