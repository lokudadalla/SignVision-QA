<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
</head>
<body>
    <h1>Sign Recognition and Question Answering System </h1>
    <p>
        This project, the <strong>Sign Recognition and Question Answering System for Hearing Impaired Individuals</strong>, aims to enhance communication for hearing-impaired individuals by combining sign language recognition with a context-aware question answering system.
    </p>
    <h2>Project Description</h2>
    <p>
        The system processes uploaded videos by breaking them down into frames and extracting images to detect hand landmarks using OpenCV. These detected landmarks enable the accurate recognition of sign language gestures, which are then translated into corresponding questions posed by the users.
    </p>
   <p>
        <img src="https://github.com/lokudadalla/SignVision-QA/blob/dfe68bdd35a858413b5b971b440a4c807e7458d1/images/1.png" alt="HandLandmark_1">
    </p>
  <p>
        <img src="https://github.com/lokudadalla/SignVision-QA/blob/dfe68bdd35a858413b5b971b440a4c807e7458d1/images/4.png" alt="HandLandmark_2">
    </p>
  <p>
        <img src="https://github.com/lokudadalla/SignVision-QA/blob/dfe68bdd35a858413b5b971b440a4c807e7458d1/images/3.png" alt="Sign_output">
    </p>
    <p>
        The context-aware Question Answering System, implemented using the BERT model transformer, interprets these questions within their given context, generating relevant and accurate responses.
    </p>
    <h2>Technologies Used</h2>
    <ul>
        <li>OpenCV for hand landmark detection and image processing</li>
        <li>BERT model transformer for the question answering system</li>
    </ul>
    <p>
        <img src="https://github.com/lokudadalla/SignVision-QA/blob/dfe68bdd35a858413b5b971b440a4c807e7458d1/images/2.png" alt="Output Answer">
    </p>
<h2>Resources</h2>
    <ul>
        <a href="https://towardsdatascience.com/question-answering-with-a-fine-tuned-bert-bc4dafd45626">Question Answering with a fine-tuned BERT (medium article)</a>
    </ul>
    <ul>
        <a href="https://www.irjmets.com/uploadedfiles/paper/issue_2_february_2022/19203/final/fin_irjmets1645622414.pdf">SIGN LANGUAGE RECOGNITION USING PYTHON AND OPENCV</a>
    </ul>
</body>
</html>
