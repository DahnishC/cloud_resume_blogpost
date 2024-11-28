# Blog Post - What I learned from the Cloud Resume Challenge
## Introduction:
When I started the Cloud Resume Challenge, I wanted to gain hands-on experience in cloud computing, web development, and continuous integration/deployment. This challenge was more than just an academic exercise; it was an opportunity to build a portfolio-worthy project that demonstrates real-world skills. By integrating multiple technologies and approaches, I aimed to prove my ability to design and deploy a scalable, cloud-based solution.

## Frontend Development: Building the Foundation
The project began with designing my resume in HTML and CSS.
HTML & CSS: I crafted a responsive, visually appealing resume hosted as a static website on AWS S3. This step emphasized the importance of web accessibility and simplicity. Using CSS, I created a clean and professional layout.
AWS S3: Hosting the website on S3 taught me how to leverage AWS’s static website hosting capabilities. The key lesson here was understanding the configuration of public access settings and bucket policies for a secure deployment.
## Ensuring Security and Accessibility
HTTPS with CloudFront and Certificate Manager: Setting up HTTPS was critical for secure communication. I used AWS Certificate Manager to generate a free SSL certificate and AWS CloudFront for content delivery, ensuring faster load times globally. This step made me appreciate the nuances of internet security and DNS management.
Custom Domain with Route 53: Configuring a custom domain added professionalism to the project. Using AWS Route 53 and Namecheap, I connected my domain with CloudFront. This integration deepened my understanding of domain registrars and DNS settings.
## Backend Development: Dynamic Visitor Counter
Creating a visitor counter required building a robust backend:
JavaScript Integration: I embedded a script to fetch and display a visitor count dynamically.
DynamoDB Database: The counter's data was stored in an AWS DynamoDB table. Setting up and querying a NoSQL database provided insights into database design and scalability.
API Gateway and AWS Lambda: Rather than connecting the database directly to the frontend, I created a secure API. The Lambda function, written in Python, handled requests and updates to DynamoDB. This layer of abstraction reinforced the importance of secure and modular architecture.
## Automating the Process: Infrastructure as Code
Terraform for Infrastructure as Code (IaC): Terraform was used to define and deploy all backend resources, including the API Gateway, Lambda functions, and DynamoDB. Learning to write and apply Terraform templates was one of the most challenging yet rewarding aspects of the project. IaC ensures repeatability and minimizes human error in deployments.
GitHub for Source Control: By maintaining separate repositories for the frontend, backend, and infrastructure, I practiced organizing and version-controlling code efficiently. Writing detailed README files enhanced documentation skills.
## Continuous Integration and Deployment (CI/CD)
GitHub Actions for Automation: I configured GitHub Actions to automate testing and deployment.
For the backend, Python tests ran upon each commit. If tests passed, the updated code was deployed to Lambda.
Terraform templates were tested and applied through another workflow.
The frontend CI/CD workflow ensured that changes to the website were automatically reflected in the S3 bucket, and the CloudFront cache was invalidated.
## Reflections on Challenges and Growth
Successfully completing this challenge demonstrated an enhanced understanding of AWS server like S3, Lambda, DynamoDB, Cloudfront, and Route 53. It also strengthened my skills in cloud infrastructure, serverless architecture, and security management through SSL certificates and HTTPS. The Cloud Resume Challenge was as much a test of resilience as it was of technical skill. Setting up the CI/CD pipelines was rough, with a a lot of time consumed of debugging. Big part of it, I realized there are many invisible characters in which you should not be copying and pasting, but one should actually type each adn every single line as it will save you so much more time compared to debugging. At the end, I have created a live product that I can showcase as part of my portfolio. 
## Next Steps
While this project marked a significant milestone, I plan to expand its scope. Future improvements include adding user authentication for the API and exploring analytics tools to track visitor engagement. The journey has only just begun.


## Conclusion
This challenge was not just about coding a resume but proving to myself and potential employers that I can deliver real-world solutions. Every service used in this project played a crucial role in creating a cohesive and scalable architecture. It’s a project I’m proud to showcase, and I’m eager to apply these skills in future opportunities.

