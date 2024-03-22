# Building-a-security-system-with-AWS-Kinesis-Rekognition...


Architecture:

<img width="858" alt="Screenshot 2024-03-22 at 09 46 43" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/ec43299d-910c-4d22-8bb9-e5cfb50be4a3">



Steps:

1. Go to Kinesis Video Streams and Create a video stream:


<img width="682" alt="Screenshot 2024-03-22 at 10 27 22" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/08a2e7a1-651e-4651-b7ce-27298f7b10be">

2. Go to IAM and create a new user AmazonKinesisVideoStreamsFullAccess
  
<img width="551" alt="Screenshot 2024-03-22 at 10 31 06" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/81526486-5fdf-4e9b-95c3-1e338e5713cb">

3. We create an S3 bucket and create a backip

<img width="685" alt="Screenshot 2024-03-22 at 10 35 56" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/abbd57a3-91c2-4eea-b997-331cc8fa21f8">

4. We launch an EC2 instance
   
<img width="604" alt="Screenshot 2024-03-22 at 10 39 10" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/d325ab7c-4748-4f1f-b2a9-3b95fabea08b">

5. We execute the commands in the Readme 2 in our terminal

<img width="805" alt="Screenshot 2024-03-22 at 10 44 34" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/4ae7b0e2-0f86-4c85-aed5-9eb7d53d2fc5">


we will send all our backups to S3:

<img width="671" alt="Screenshot 2024-03-22 at 10 48 40" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/86a8d800-e56d-495d-b4ba-39e77c3eddb1">

We stream data from a webcam and receive the data from my consumer:

<img width="1357" alt="Screenshot 2024-03-22 at 10 50 22" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/3119d16b-020f-4272-8e68-3e1a8a877bf7">

we create another s3 bucket for detections:

<img width="911" alt="Screenshot 2024-03-22 at 10 56 11" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/533c7259-f41c-477e-a65d-a21ab84afab1">

we go to DynameDB and create a table:

<img width="862" alt="Screenshot 2024-03-22 at 10 57 07" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/b0355906-7f7e-45d9-bc89-1e32bc4bf2a9">

we go to SNS and create a Topic to create notifications to an email:

<img width="714" alt="Screenshot 2024-03-22 at 10 58 46" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/369ee08d-f194-48de-a591-1d74265d1f5c">

we confirm the subscription:

<img width="448" alt="Screenshot 2024-03-22 at 10 59 35" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/ea37f555-021f-4222-8a32-c296aaf7192f">

we create a notification on the "Intruder-detection-tutorial-bucket"

<img width="697" alt="Screenshot 2024-03-22 at 11 01 47" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/4cb52213-4027-4092-9d1c-d8b826d14993">

<img width="721" alt="Screenshot 2024-03-22 at 11 03 24" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/fc560d5d-35f8-4baf-b496-88665d8c76a1">

we launch an instance and we attach all these policies:

<img width="800" alt="Screenshot 2024-03-22 at 11 05 26" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/44226be7-257b-4923-a202-ae3ad811398d">

we create a new role and attach it to the ec2 instance:


<img width="692" alt="Screenshot 2024-03-22 at 11 07 10" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/3c80453e-0506-4fee-ab9a-9c764b8ab194">

<img width="736" alt="Screenshot 2024-03-22 at 11 07 37" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/51280bb0-4bd5-4f97-b383-27d98639f18a">

<img width="646" alt="Screenshot 2024-03-22 at 11 10 05" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/aca49f95-f83c-4497-9d21-ebfcce4bab4a">

<img width="1355" alt="Screenshot 2024-03-22 at 11 20 37" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/97ffcfda-5802-41bb-b4f6-ba29189d5281">

<img width="1276" alt="Screenshot 2024-03-22 at 11 21 52" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/225e7150-6e13-4cd1-ac23-8c1d8bd8c630">


we are receiving backups:

<img width="514" alt="Screenshot 2024-03-22 at 11 24 24" src="https://github.com/redjules/Building-a-security-system-with-AWS-Kinesis-Rekognition...-/assets/106017493/c46951a3-c01d-4179-b161-c2130c7a176a">


