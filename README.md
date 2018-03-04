# rest-api-development

CS5331 Assignment 1 Project Reference Repository

## Instructions

Your objective is to implement a web application that provides the endpoints
specified here: https://cs5331-assignments.github.io/rest-api-development/.
# Screenshots

Please replace the example screenshots with screenshots of your completed
project. Feel free to include more than one.

![Sample Screenshot](./img/samplescreenshot.png)

## Administration and Evaluation

Please fill out this section with details relevant to your team.

### Team Members

1. LAU Wee You
2. LEE Zi Shan
3. SIA Wei Kiat Jason
4. ZHOU Zhi Zhong

### Short Answer Questions

#### Question 1: Briefly describe the web technology stack used in your implementation.

The application uses Python-Flask to handle requests to the back-end. The code in the Python-Flask will then modify our database using SQLite3. 

On the UI, we use javascript to asynchronously call our RESTful API and modify our HTML accordingly.


#### Question 2: Are there any security considerations your team thought about?

Yes. However, given that it is not part of the requirements, we have not implemented them. 

Sanitization of inputs should be implemented so that user cannot conduct injection attacks such as SQL-Injection and XSS. For example, without sanitisation, user can write a simple script in a public entry

Password protection considerations such as limiting the number of login attempts, password checkers to check for weak passwords. 
 
#### Question 3: Are there any improvements you would make to the API specification to improve the security of the web application?


#### Question 4: Are there any additional features you would like to highlight?

Answer: Please replace this sentence with your answer.

#### Question 5: Is your web application vulnerable? If yes, how and why? If not, what measures did you take to secure it?

Answer: Please replace this sentence with your answer.

Yes, the web application is vulnerable. 
1) There is a chance of leaked session ID. Hence to be more defensive, We store session data such as token on the server side in our Users table. Every login, we will generate a new token and this token will be tagged to the current user for the particular session.

2) 









#### Feedback: Is there any other feedback you would like to give?

Answer: Please replace this sentence with your answer.

### Declaration

#### Please declare your individual contributions to the assignment:

1. LAU Wee You
    - Implemented z
2. LEE Zi Shan
    - Implemented z
3. SIA Wei Kiat Jason
    - Implemented z
4. ZHOU Zhi Zhong
    - Implemented z



/* Actual Document Starts Here*/

Database Schema

Table
users {
  username: varchar (255) not null,
  fullname: varchar (255) not null,
  salt: varchar (255) not null,
  hashed_password: varchar (255) not null,
  age: int not null
}

diary_entries {
  id: int primary key auto increment, 
  title: varchar (255) not null,
  author: varchar (255) not null,
  publish_date: datetime not null, 
  public: boolean not null, 
  text: text

}

members {
  name: varchar (255) not null
}
