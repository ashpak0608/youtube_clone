# 🎬 YouTube Angular-Node Full Stack Project

This is a **full stack project** built with:

- **Frontend:** Angular  
- **Backend:** Node.js with Express and Prisma ORM (using MySQL/MariaDB database)

---

## 📁 **Project Structure**


youtube/
├── backend/ # Node.js + Prisma backend
├── src/ # Angular frontend source code
├── package.json
└── README.md


---

## 🚀 **Setup Guide**

### ✅ **Prerequisites (Install these first)**

1. **Node.js** (v14 or higher recommended)  
   [Download Node.js](https://nodejs.org)

2. **npm** (comes with Node.js)

3. **Angular CLI**

Install Angular CLI globally if not installed:

Frontend Project complete setup : 

1. git clone git@github.com:ashpak0608/youtube_clone.git            //for linux machine 
2. git clone https://github.com/ashpak0608/youtube_clone.git        //for windows machine

3. cd youtube

4. npm install -y

5. npm install -g @angular/cli                                 //optional if not installed with package.json

6. ng serve                                                   // to run the project frontend

7.  http://localhost:4200/                                  // bydefault it will hit this url



Backend project setup : 

1. Configure database connection

Open your .env file in the backend folder.

Update "DATABASE_URL" with your MySQL/MariaDB credentials. Example:

DATABASE_URL="mysql://username:password@localhost:3306/databasename"        //if the .env file is not present generate using command "npx prisma init".

Replace:

username with your DB username (e.g. root or myuser)

password with your DB password

databasename with your database (e.g. logindata)


2. npx prisma migrate dev --name init                          // Create tables in your database based on your Prisma schema.

3. node index.js                                               //this will run the project 

4. http://localhost:3000/                                      //url will hit this 


5. Testing the Backend API with Postman

Open Postman.

Create a new POST request.

URL: http://localhost:3000/login

Headers: Content-Type: application/json

Body (raw JSON):

{
  "username": "testuser",
  "password": "testpass"
}
Click Send to test the API.





*Final Steps to Run Both Projects
Start your database server (MySQL/MariaDB)*

Run backend server:

cd backend
node index.js
Run frontend Angular app:

cd youtube
ng serve