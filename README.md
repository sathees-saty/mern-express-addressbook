# mern-express-addressbook

<html>
<hr>
Database :
</hr>
<br>
•	For database we are using local MongoDB.
<br>
•	Inside MongoDB create a new database with the name ‘addressbook’.
<br>
•	Now create ‘addresses’ collection inside this database and we are done with database part.
<br>
D:\express-development\mern-addressbook


<br>
Frontend:
<br>
Step 1: First we will create a frontend for our application in React . start a new react project using below command .
<br>
npx create-react-app address-book
<br>
Step 2: For this project we will require axios to make API calls to backend . Also we will require bootstrap for elegant design . We are also going to use react-bootstrap-icons for icons . finally we will use react-router-dom package for routing in frontend.
<br>
Step 3: Install all the dependencies using npm as below inside frontend folder.
<br>
D:\express-development\mern-addressbook>cd address-book
<br>
npm i axios react-bootstrap-icons react-router-dom
<br>
Step 4: For bootstrap get CDN links of bootstrap and jquery and paste it inside index.html file in public folder as below.
<br>
<link href=”https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css” rel=”stylesheet” integrity=”sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC” crossorigin=”anonymous”>
<script src=”https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js” integrity=”sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM” crossorigin=”anonymous”></script>
<script src=”https://code.jquery.com/jquery-3.7.1.min.js” integrity=”sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=” crossorigin=”anonymous”></script>
<br>
Step 5: Create a folder called components in src directory and create files AddAddress.js, AddressList.js, Navigation.js inside it. - Created
<br>
Backend
For backend create a separate folder outside of React folder called ‘address-book-backend’.
<br>
D:\express-development\mern-addressbook>mkdir address-book-backend
<br>
D:\express-development\mern-addressbook>cd address-book-backend
<br>
D:\express-development\mern-addressbook\address-book-backend>
<br>
Step 1: Inside this folder initiate node project using below command.
<br>
npm init
<br>
Step 2: Now lets install required packages nodemon , express , mongoose , cors , body-parser as below:
<br>
npm i express nodemon mongoose cors body-parser
<br>
Step 3: Once the packages are installed create a app.js file which will contain our backend code . Also create a folder models and create a file address.js
<br>

Steps to run the application :
<br>
Steps for running backend code :
Step 1: For running application first lets add start script inside package.json of backend. add line for nodemon start script.
<br>
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon app.js"
}
<br>
Step 2: Open another terminal inside backend folder and run below command. 
<br>
npm start
<br>
//await Address.findByIdAndRemove(req.params.id); - not working in backed API
<br>
await Address.findOneAndDelete(req.params.id); // working 
<br>
Steps for running frontend code :
<br>
Step 1: Open terminal inside frontend folder and run below command . (before starting frontend server, start backend server)
<br>
npm start 
<br>
Step 2: The browser will automatically open tab with home page. http://localhost:3000/
</html>
