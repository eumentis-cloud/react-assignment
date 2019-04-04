# Eumentis Cloud - ReactJS assignments

Here we provide the instructions for developing two ReactJS applications, designed by the Eumentis Cloud team, to test the proficiency of applicants for the ReactJS Frontend Developer position(s):

* **Assignment 1 - Beginner**: For applicants who have just learned React and have minimal to no experience in developing application using React.
* **Assignment 2 - Advanced**: For applicants who have a good working knowledge of React and have worked on / developed at least one React application

All applicants are required to submit only one assignment based on their knowledge, experience and confidence in ReactJS. We advice applicants to see the demo and instructions for both the assignments before deciding which one to submit.

## Prerequisites
* Knowledge of ReactJS (obviously), HTML, CSS, Bootstrap (optional, but will be really helpful for Assignment 1)
* Knowledge of installing npm packages (both local & global)
* Knowledge of creating React application using [Create React App](https://facebook.github.io/create-react-app/)
* Knowledge of fetching JSON data from a REST API endpoint
* A Github account in order to share his/her code with us

## Submission guidelines

### Sharing the code

All applicants must share their code in one of the following ways:

 - Upload their code on their Github account by creating a public repository and sharing the link via email.
 - Creating a zip file of their project folder (excluding the node_modules directory) and either uploading it to a cloud service (sharing the link with us) or attaching it to an email (if size < 20 MB).

### Deploying the code for testing

All applicants are also required to deploy their assignment to a server or to any of the static hosting service providers ([link to help with deployment](https://facebook.github.io/create-react-app/docs/deployment)).

#### Deploying React apps with [Zeit Now](https://zeit.co/now)

For applicants who have no experience with deployments, please follow the instructions below for deploying React apps with Zeit Now.

1. Create an account on Zeit Now ([signup link](https://zeit.co/signup))
2. Install the Zeit Now npm package globally: `npm i -g now`
3. Go to your project's root directory and build your react application: `npm run build`
4. Go into the build directory created in last step: `cd build`
5. Log into your Zeit Now account (created in step 1) by following instructions presented by running the command: `now login`
6. Deploy your application (you should be in the build directory of your app): `now --name <firstName>-<last-name>`. For example, if a person's name is 'Pawan Samdani' he should run this: `now --name pawan-samdani`

## Assignment Details

Both the assignments (Beginner & Advanced) are frontend React applications with no backend development required.

The idea of both the assignments is to build a single page that displays the profile of 10 users (the data is obtained from an API endpoint). Each user's profile contains a avatar picture, name, email, phone, address, website and company name.

#### API endpoint for users data

All 10 users profile data is to be downloaded from the following API endpoint:
```
Method: GET
URL: https://jsonplaceholder.typicode.com/users
```

The schema of the data received in the response is:
```Javascript
// Array of 10 users
[
  {
    id,	// The user's id
    username,
    name,
    email,
    phone,
    website,
    address: {
	  street, // Address line 1
	  suite, // Address line 2
	  city,
	  zipcode
    },
    company: {
	  name, // The name of company where the user works
    }
  }
]
```

#### API endpoint for users' avatar pictures

You will be using [Avatars by DiceBear](https://avatars.dicebear.com/). They provide a free HTTP API to create unique avatar images based on any string we send as query parameter. Each string generates a unique image. You will use the `username` to generate a unique avatar for each user.

The URL for the `GET`  endpoint is:
```
https://avatars.dicebear.com/v2/avataaars/{{username}}.svg?options[mood][]=happy
```

The `{{username}}` in the URL is the placeholder for the user's username. It should be dynamically replaced by the username received from the users API endpoint. For example, if the username for one of the users is `psamd` then the URL for the avatar for this user will be: `https://avatars.dicebear.com/v2/avataaars/psamd.svg?options[mood][]=happy`

#### Loading Indicator

Upon opening the app a loading indicator is displayed until the data is fetched from the API and is ready to be displayed. The source code for the loading indicator can be obtained from: [http://tobiasahlin.com/spinkit/](http://tobiasahlin.com/spinkit/).

## Assignment 1 - Beginner

**Deadline for submission:** 3 days

DEMO - https://react-basic-assignment.psamd.now.sh/

This assignment is designed for applicants who have learned ReactJS and have minimal hands-on experience in developing react application.

### What are we looking for?

With this assignment we would evaluate the following:

 - Ability to create new react projects using [Create React App](https://facebook.github.io/create-react-app/)
 - Understanding of JSX
 - Passing props to components
 - Understanding of stateful and stateless Components
 - Basic understanding of state management and component lifecycle methods
 - Fetching data from an API endpoint
 - Conditional rendering
 - Working with lists

### Instructions

We want applicants to create an exact replica of the [assignment 1 demo app](https://react-basic-assignment.psamd.now.sh/).

This app is only designed for desktop/laptop and will be tested on Chrome browser.

Bootstrap was used to create the UI design for the demo app. But, applicants are encouraged to use any other CSS library/framework that they are comfortable with.

## Assignment 1 - Advanced

**Deadline for submission:** 7 days

DEMO - [https://react-advanced-assignment.psamd.now.sh/](https://react-advanced-assignment.psamd.now.sh/)

This assignment is designed for applicants who have a good knowledge and understanding of React and have developed/worked on atleast one React application.

### What are we looking for?

Everything mentioned in the Assignment 1 and additionally:

 - Ability of the applicant to learn a new React UI library and use its components in their app
 - Handling events and working with forms
 - [Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)

### Instructions

We want applicants to create the closest possible replica of the [assignment 2 demo app](https://react-advanced-assignment.psamd.now.sh/).

This app should be a responsive (mobile, tablet and desktop) and will be tested on Chrome browser.

The entire app was designed using the [Ant Design](https://ant.design/) library. It is mandatory for applicants to use the library to design the Icons, Buttons, Cards, Grid, Modal and Form in the demo app.

## General Tips

 - Feel free to use Google, StackOverflow or any other resource
 - Examine the demo apps closely to determine all the features
 - Open the data API link in your browser and examine the response schema
 - For applicants attempting the Assignment 2, please read the documentation of [Ant Design](https://ant.design/docs/react/introduce) library carefully and thoroughly.
 - Try to match the UI design of the demos for each assignment as closely as possible.
 - Please feel free to get in touch with the Eumentis Cloud's team to clear any doubts related to the aforementioned instructions.
