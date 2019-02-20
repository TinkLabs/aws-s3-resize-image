# aws-s3-resize-image
S3 based image processing service


In order to ensure the high availability of the image service, we will store all the images (including the original image and the thumbnail image) in AWS's object storage service S3 and deploy the image processing program in AWS EC2. Most of the image requests will be returned directly by AWS S3. Only when there is no required thumbnail graph in S3, will the image processing service deployed on EC2 be requested to generate the corresponding resolution image.