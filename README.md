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

## Git - Removing Sensetive Data

Mistakes happen. On a version control system like git, there will be a time when a sensetive information is commited to a repo, e.g. a password, Personal Identifying Information, etc. This [guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) on Gthub introduces two options to fix such mistake. The idea, as far I as I can tell, is to rebuild the repo with mistakes removed, e.g. There will be similar cmmits but with different hash codes. Here is my experience with the two methods:

1. [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/): A ```jar``` file that requires a Java Runtime Environment. In addition to removing sensetive files, it allows to replace sensetive texts with a generic text ```***REMOVED***```. The instruction on Github was slightly different with the package's website. I managed to install and run the command, however I ran into error when it came to pushing the changes back to Github. I found some potential reasons and fixes, but before spending too much time I tried the 2nd option, which worked like a breeze.

2. [git filter-repo](https://github.com/newren/git-filter-repo): A ```python``` file that requires Python3. With the alias ```git-filter-repo``` pointing to ```python3 /path/to/downloaded/git-filter-repo```, the steps to remove the sensetive file was as simple as this:

```bash
git clone https://github.com/myusername/myrep.git
cd myrepo
git-filter-repo --invert-paths --path path/to/sensetive/file
git remote add origin https://github.com/myusername/myrep.git
git push origin --force --all
```

## C#, .NET, and ASP.NET

[.NET](https://dotnet.microsoft.com/en-us/learn/dotnet/what-is-dotnet) is an open-source and cross-platform framework created by Microsoft for software development. [ASP.NET](https://en.wikipedia.org/wiki/ASP.NET) is a framework for building dynamic web applications with `.NET` and `C#`. [C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)) is a programming language that can be used to utilize frameworks like`.NET` and `ASP.NET`. A summary note on installation and sample codes added to [this page](https://github.com/ghasimi/notebook/blob/dotnet/dotnet.md). 


