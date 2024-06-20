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
        <img src="https://private-user-images.githubusercontent.com/133969661/341421863-1967cd36-0182-4d2c-acd8-f844136bbe98.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTg4ODk5MzYsIm5iZiI6MTcxODg4OTYzNiwicGF0aCI6Ii8xMzM5Njk2NjEvMzQxNDIxODYzLTE5NjdjZDM2LTAxODItNGQyYy1hY2Q4LWY4NDQxMzZiYmU5OC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyMFQxMzIwMzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0yNWM3M2NjMDcwMWFjZWYxMTU0ODc5YTJlNzc1YmI1YzU1YWZhMmIyOTFlNTA2ZjU3YWIwNGE4ZTYxMDQyMDU3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.5ydEY5K31kHAZwtqfVTWIdvjFWVOn8Qz6sIm7VVQYsw" alt="HandLandmark_1">
    </p>
  <p>
        <img src="https://private-user-images.githubusercontent.com/133969661/341423319-82d21a7c-7a7c-4204-b1d8-ee974e5e1b87.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTg4ODk5MzQsIm5iZiI6MTcxODg4OTYzNCwicGF0aCI6Ii8xMzM5Njk2NjEvMzQxNDIzMzE5LTgyZDIxYTdjLTdhN2MtNDIwNC1iMWQ4LWVlOTc0ZTVlMWI4Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyMFQxMzIwMzRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZmNhYzdmMTExNGViZWJkZmRiZTg3MTQwM2FiNjMzMDhlYWRlYjk4ZTM1MzMwZTMwOGMyMWRkNGI2OGVlZGVhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.mxY5hBF0VisE-cfM-vgT8kd6ilMOnI0X95xZ7tqagpM" alt="HandLandmark_2">
    </p>
  <p>
        <img src="https://private-user-images.githubusercontent.com/133969661/341423065-07f7b7d7-a9e7-4656-a77a-30a1377906bc.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTg4ODk5MzYsIm5iZiI6MTcxODg4OTYzNiwicGF0aCI6Ii8xMzM5Njk2NjEvMzQxNDIzMDY1LTA3ZjdiN2Q3LWE5ZTctNDY1Ni1hNzdhLTMwYTEzNzc5MDZiYy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyMFQxMzIwMzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZWU4YjJiNDUyZWZjZWZmYjczZGE5ODRmMTVmNmMzZTg0NTk4ZDkwYmMwNjcwNzM3NmJlMDU0MDdlMzk4YTk5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Vln64vm7CmMLuyGO8PC_F2-sS_iL8yCr0jTvIWzNDds" alt="Sign_output">
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
        <img src="https://private-user-images.githubusercontent.com/133969661/341423046-6e5ce746-9f23-4b92-8214-539e6c4ea05c.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTg4ODk0NjksIm5iZiI6MTcxODg4OTE2OSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQxNDIzMDQ2LTZlNWNlNzQ2LTlmMjMtNGI5Mi04MjE0LTUzOWU2YzRlYTA1Yy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyMFQxMzEyNDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04MDhiYmQ2YWQ2MjU4Y2MwODI1NmEzOTEwMjNhYTY3YTdmZTFjYWUxYzYxMWEyNDVmOGE5NDVjNTdiOWQ0NmFmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.2n-ZrjEPTZFtUOH4AMcc3NiT_8zae4KlOnu8P1-u9SA" alt="Output Answer">
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
