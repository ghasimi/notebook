# notebook
A place for random notes and ideas.

## CI/CD and DevOps

Notes from a short and useful article by [Suzie Prince](https://www.mindtheproduct.com/what-the-hell-are-ci-cd-and-devops-a-cheatsheet-for-the-rest-of-us/):

- Continues Integeration (CI): When developers frequently check-in to the main repo. When tests pass they get a green build. 

- Continues Delivery (CD): Automatically deploy and test in an environment that is very similar to the production. The deployment pipeline typically includes dev, test, and staging environments. Deployment to the prod is still __manual__. 

- Continues Deployment (CD): Here, in contrast to the Continues Delivery, the deployment to the prod is __automatic__.

- CI/CD: The CI part is clear, and the CD part determines whether it is Continues Delivery or Deployment. Unit test is a prerequisite of CI/CD.

- DevOps: A culture that "promotes collaboration between the developers and other technology professionals, often called operations or just ops".  

<img  
  alt="I/CD" 
  src="https://wac-cdn.atlassian.com/dam/jcr:b2a6d1a7-1a60-4c77-aa30-f3eb675d6ad6/ci%20cd%20asset%20updates%20.007.png?cdnVersion=573" 
  style="width:650px;"
  />
  
CI/CD image credit: atlasian.com, [Sten Pittet](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)    
