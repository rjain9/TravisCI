# CSC 519 TechTalk - TravisCI

## Team Members:
* Rishi Jain (rjain9)
* Shriyansh Yadav (scyadav)
* Omkar Acharya (oachary)
* Urmil Parikh (uparikh)

## [Presentation Slides](docs/slides.pptx) | [Travis CI Demo]() | [Demo Code]()

## Introduction
### What is Travis CI?
It is a hosted, distributed continuous integration service used to build and test software projects hosted at GitHub.

### What are its functionalities?
* Build artefacts
* Run Tests
* Provide feedback
* Deploy to cloud services

### How does it work?
![How does it work](img/workflow.jpg)

### What are some pros and cons of Travis CI?
* **Pros:**
  * Variety of collection of plugins
  * Free to use for public project
  * Easy for customization
* **Cons:**
  * No manual builds
  * No build pipelines
  * Need to rely on their on their infrastructure
  * Less extensible not suitable for high security projects

### Other CI tools
![Other CI tools](img/ci_tools.png)

### Our view on Travis CI


### Setup Instructions
* Create a new GitHub repository or clone it from remote
```
git clone https://github.com/rjain9/TravisCI.git
cd TravisCI
```
* Add `.travis.yml` script at the root of the repository
  * Specify the programming language 
  * Desired building and testing environment
  * Dependencies for those environments
  * Other parameters, if any
```
language: java
sudo: false
script: mvn test
```
* Sign in to [Travis CI](https://travis-ci.org) using GitHub credentials
* Select `Add new repository (+)` from `Dashboard` and enable integration for the repository
* Make some changes in the local repository
```
git add <files>
git commit -m <message>
git push origin <branch>
```
* This will trigger a new build and you can see that on Travis CI's dashboard
