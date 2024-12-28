# Steps to follow to run web application

# Step1: Extensions in VSCode
1. Better Comments
2. Bootstrap 5 Quick Snippets
3. Code Runner
4. MySQL
5. GitHub Codespaces
6. GitLens Git supercharged
7. HTML Boilerplate
8. HTML CSS Support
9. JavaScript(ES6) code snippets
10. Live Server
11. pylance
12. python
13. python Debugger

# Step2: Install the packages 
Command: `pip install -r requirements.txt`

# Step 3: Install the MYSQL
1. **In system:**
	
 	You cannot directly "install" MySQL Server within Visual Studio Code (VS Code) /windows.
By following this link: https://youtu.be/a3HJnbYhXUc?si=h0PXHuO0sQ94MEyR
2. **In Codespace:**

	By following this GitHub link: https://chatgpt.com/share/676f9c6b-e8a4-8008-9260-bc8caec8d0a2

# Step 4: Create DataBase and Tables

**command to be run in MYSQL shell:**

- `CREATE DATABASE charity;`

- `use charity;`

- ```CREATE TABLE `charityinformation` (
  `Slno` int(100) NOT NULL AUTO_INCREMENT,
  `Charityname` varchar(200) DEFAULT NULL,
  `Charityemail` varchar(200) DEFAULT NULL,
  `Charitypassword` varchar(200) DEFAULT NULL,
  `Charityaddress` varchar(200) DEFAULT NULL,
  `Charitycontact` varchar(200) DEFAULT NULL,
  `status` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`Slno`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4;```

- ```CREATE TABLE `donation` (
  `Slno` int(200) NOT NULL AUTO_INCREMENT,
  `Charityname` varchar(200) DEFAULT NULL,
  `Charityemail` varchar(200) DEFAULT NULL,
  `Charityaddress` varchar(200) DEFAULT NULL,
  `Useremail` varchar(200) DEFAULT NULL,
  `status` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`Slno`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4;```

- ```CREATE TABLE `transactiondetails` (
  `Id` int(200) NOT NULL AUTO_INCREMENT,
  `Charityemail` varchar(200) DEFAULT NULL,
  `CharityaccountNumber` varchar(200) DEFAULT NULL,
  `charityifsccode` varchar(200) DEFAULT NULL,
  `Userename` varchar(200) DEFAULT NULL,
  `usercardnumber` varchar(200) DEFAULT NULL,
  `expiredate` varchar(200) DEFAULT NULL,
  `cvv` varchar(200) DEFAULT NULL,
  `amount` varchar(200) DEFAULT NULL,
  `status` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`Id`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8mb4;```

- ```CREATE TABLE `userinformation` (
  `Id` int(200) NOT NULL AUTO_INCREMENT,
  `Username` varchar(200) DEFAULT NULL,
  `useremail` varchar(200) DEFAULT NULL,
  `password` varchar(200) DEFAULT NULL,
  `age` varchar(200) DEFAULT NULL,
  `contact` varchar(200) DEFAULT NULL,
  `address` varchar(200) DEFAULT NULL,
  `Status` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`Id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4;```

# Step 5:Connect server

By providing the password of (root)user of MySQL server in `app.py file`.

**Example:**
	```db=mysql.connector.connect(user='root',host='localhost',
			                    password='your_password',
				                  port=3306,database='charity')```

# step 6: Run application
1. Run application in terminal by Command : `python app.py`
2. Click on the output link after running the program open in browser
