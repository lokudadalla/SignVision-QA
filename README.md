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
        <img src="https://private-user-images.githubusercontent.com/133969661/358854271-1566f287-ffff-4439-ae52-d32801bfbb20.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjM5MDkwMjQsIm5iZiI6MTcyMzkwODcyNCwicGF0aCI6Ii8xMzM5Njk2NjEvMzU4ODU0MjcxLTE1NjZmMjg3LWZmZmYtNDQzOS1hZTUyLWQzMjgwMWJmYmIyMC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwODE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDgxN1QxNTMyMDRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iMTdmZTFiZmRmYjIzMjVmYTRjOGI3M2NlOTc4Y2Q5MjVkYTdhM2QzMmRiNjA5NDc1MWVlNGM1YzRjZWUxNThiJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Yn0fcv7fAjDyc7CKYxi0GdfrZhPJA8wjTwXRyiD0uPI" alt="HandLandmark_1">
    </p>
  <p>
        <img src="https://private-user-images.githubusercontent.com/133969661/358854361-d79ed8b4-5742-44bd-8e82-f63384b16dd3.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjM5MDkwMjQsIm5iZiI6MTcyMzkwODcyNCwicGF0aCI6Ii8xMzM5Njk2NjEvMzU4ODU0MzYxLWQ3OWVkOGI0LTU3NDItNDRiZC04ZTgyLWY2MzM4NGIxNmRkMy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwODE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDgxN1QxNTMyMDRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNmU5YTkxMWI4NTQzOTdjZWJlYmU1OGRhN2IwMmI0YmQ0NTY5ZjhjNmRkOTdkYTgxODhhYWQ0MzFiYmNkMDJmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.1oB2hJayvOfVN0YeVWaXgFZfrKGc0KEhphzjC0orLWQ" alt="HandLandmark_2">
    </p>
  <p>
        <img src="https://private-user-images.githubusercontent.com/133969661/358854279-54b8cdc0-9817-466f-81f4-d5d080dc8808.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjM5MDkwMjQsIm5iZiI6MTcyMzkwODcyNCwicGF0aCI6Ii8xMzM5Njk2NjEvMzU4ODU0Mjc5LTU0YjhjZGMwLTk4MTctNDY2Zi04MWY0LWQ1ZDA4MGRjODgwOC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwODE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDgxN1QxNTMyMDRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zNmE2YmMzYTc1YzZmYTAyMGQ0OTc1MmZmNTQxMDg0NzQxMmZjNzYxN2I4MTBmZjRhYjA2NzExODI1YzM2Y2IxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.1AzS7f12kumalhTxgsE4fitYzpC6coYpElYWLpyCUCM" alt="Sign_output">
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
        <img src="https://private-user-images.githubusercontent.com/133969661/358854284-4568ba66-a155-4efc-9c5c-082878c72cba.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjM5MDkwMjQsIm5iZiI6MTcyMzkwODcyNCwicGF0aCI6Ii8xMzM5Njk2NjEvMzU4ODU0Mjg0LTQ1NjhiYTY2LWExNTUtNGVmYy05YzVjLTA4Mjg3OGM3MmNiYS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwODE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDgxN1QxNTMyMDRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jYWQwOTQ2NGY1Y2EyN2IzMDViYmQ2NGI3MTYxZmJiMTRjYTcxNzgwNzE2ODM0Nzk5MTJlMTY4YWQ0ZDRhYzk5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.k9DoXQ_by32IyIQ9VCoX5jakYpqVNK9X4DhUlENhDLs" alt="Output Answer">
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
