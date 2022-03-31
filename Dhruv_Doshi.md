# WeCare Solutions

One place solution for all the hospital management needs. Web App which provides access to patient and doctors both and have multiple utilities like Careers, Blogs, Bookings and many more.

Gitlab: https://git.cs.dal.ca/choksi/webproject/
Heroku: https://csci5709-group9.herokuapp.com/

Credit: Harivansh Bhatiya for Heroku

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them, given is for Linus systems for Windows it is suggested to use Windows subsysten for Linux version 2.

```
sudo apt-get install node@lts
```

### Installing

A step by step series of examples that tell you how to get a development env running

Need to Clone the Code and run backend and frontend on different terminals

```
git clone https://git.cs.dal.ca/choksi/webproject/
cd webproject
```

Running Backend API
```
cd backend
npm install 
npm start
```

Running Frontend API
```
cd ..
cd frontend
npm install 
npm start
```


## Deployment

THe application could be deployed in multiple ways with Heroku, Vercel, Github Pages or EC2.
The application is already deployed with <a href="https://csci5709-group9.herokuapp.com/"> link </a>


## Built With

* [React](https://reactjs.org) - The web framework used
* [Node](https://nodejs.org/en/docs/) - Node JS for development
* [Express](https://expressjs.com) - Running Backend API
* [MongoDB](https://www.mongodb.com) - Database Utilization


## Authors

* Dhruv Doshi(Dhruv@dal.ca) - *(Developer)*

## Files created 

Single author for all the files - required for the functioning of career page.

1. /backend/controllers/careerController.js
2. /backend/models/careerModel.js
3. /backend/routes/careerapiRoutes.js
4. /backend/routes/careerauthRoutes.js
5. /backend/routes/careeruploadRoutes.js
6. /frontend/src/components/career/Applications.js
7. /frontend/src/components/career/Home.js
8. /frontend/src/components/career/Login.js
9. /frontend/src/components/career/Logout.ks
10. /frontend/src/components/career/apiList.js
11. /frontend/src/components/career/isAuth.js
12. /frontend/src/components/career/recruiter/AcceptedApplicants.js
13. /frontend/src/components/career/recruiter/createjobs.js
14. /frontend/src/components/career/recruiter/jobapplicants.js
15. /frontend/src/components/career/recruiter/myjobs.js
16. /frontend/src/components/career/recruiter/profile.js


## Individual Module

* Feature 1: Carrer Page User side
* Feature 2: Carrer Management Recruiter Side

Feature 1 is complete and most of the feature, for Feature 2 is also working.

Career module was one of the portion of the project which needed to be isolated from the existing application. At the time of the ideation phace we continued with the simpel login module whihc could be used acroos the application.
But there is no need for the nieve user to access the information which is just relevant for the job seeker or finder.

We checked multiple corporations which have the carrer page inside the application but we found that most cases they were completely isolated from the exisitng systems.

Like for applying to Amazon or Facebook we need to make another accounts at either Meta careers or Amazon University hence we came up with the module in which the code is tightly integrated within the existing app but hosted with different domain.

This called for restructing and redoing the whole flow of the system but came up with several benefits like,
 - Limited scope and exposure to the application
 - Easier Navigation for the Applicant
 - Easy Management of the Files and no heavy uploaded files on main server

Developing this alternative way the whole application was esclaped in the single repository but it allowed us to have future scope to get the resume and save it as this specific part was deployed with EC2 Instance which would allow us to have EBS or S3 in which these files could be stored of Instead of MongoDB.


## Overview

Here is an overview which shows that how to register using the MERN app.
<div align="center">

![MERN APP LOGIN](https://github.com/DhruvDoshi/public-gif/blob/master/Login.gif)

</div>
This is just an GIF which shows that how to look into the application and how to deal with the interface.

As mention before there had been significant changes within the proposed approach and at the end of the developemnt it is evident that the alternative solution which had been used is more better.



## Code Integration Steps
1. Started with devlopment of individual features by putting the blank react app on the mail.
2. Every member made their own branch or had an option to develop of other repo and then push to the branch of their choise.
3. The basic application was developed by sanika tomar, she was in charge of user management and the authorisation module. Everyone contacted her and she managed the routing of all the application.
4. As my module used working with the .pdf files and we were not allowed to directly use any pre developed API hence my module needed to be hosted with the space where files could be stored of hence the backend was hosted on ec2 server and then it was integrated with the main system.
5. There were multiple merge conflicts which resulted due to our mistake of nut doing fresh pul before the push but we all sat together before the deadline and one by one merged everyone's code in the master repository.
6. This was one of the most time consuming part for the development as the deployment was failing continously when there was a single error. Still be continued and finally we did it.

## Learnings
1. Never push the code before fresh pull.
2. Always stash the code as it will save the copy.
3. It is easy to use heroku cli for the deployment but prefer the pipeline which automates the deployment.
4. Always have the node test and the buils stage in the pipeline which would reject the merge or commit if the app if failing.
5. Prefer EC2 or any other linux server for the deployment of the application over heroku or vercel. They do not provide the interactive bash which results in issues solving the error.




There are multiple Job posts whicha re up and there are multiple users which had applied for the job. the application is well running and there is no random information within the application. Here are some screenshots and relevant information.







<div align="center">

![Job Board for Applicant](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.34.00%20PM.png)


![Job posted by Recruiter](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.35.29%20PM.png)


![User Applying with SOP](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.44.05%20PM.png)


![Application shown on Recruiter end](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.45.44%20PM.png)


![Shortlisted for the job](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.46.18%20PM.png)


![Accept or reject the Job](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.46.36%20PM.png)


![Accepted on Recruiter Side](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.46.54%20PM.png)


![Reflected on User Side](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.47.10%20PM.png)


![Job rating by User](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-29%20at%204.48.12%20PM.png)

<br>

Dashboards for EC2 and MongoDB deployment

![EC2 Dashboard](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-31%20at%203.15.43%20PM.png)


![MongoDB](https://github.com/DhruvDoshi/public-gif/blob/master/Screen%20Shot%202022-03-31%20at%203.16.08%20PM.png)



</div>

Please find the code for the feature along with the master repository of the whole application. Everything is completely integrated with the application.
For any other information please ping me on slack or Dhruv@dal.ca. Looking forward for your feedback.