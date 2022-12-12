
#implementation of cyber security technologies in ASMIS

A brief description of what this project does and who it's for

This document is aimed to provide explanation and rationale for implementation of cyber security technology for a web-based appointment scheduling and management information system (ASMIS). 

Background: 

Queens Medical Centre is facing a high number of calls for appointment booking which the facility is unable to handle because of growing size of the population in the catchment area. The clinic management has decided to introduce web-based appointment scheduling and management information system.  

While developing ASMIS, multiple vulnerabilities can be detected and if exploited can lead to data leaks which can cause negative implications to the organization and individuals. The first vulnerability (which is addressed in the solutions below) was to stop cyber attackers from gaining access to the system, which can be done by knowing the username and password through brute force attacks, phishing, malware or social engineering. One of the proposed solutions is to implement multifactor authentication through one time password which adds an extra layer of security to make sure an authentic user is logging in. The second measure is to encrypt and decrypt the user's logging details to securely store the information. The second measure is to implement password hashing which stores the user’s passwords into hash value instead of a plain text which is difficult for the cyber attackers to hack. 

The python project attached with this file applies the use of python code to implement the multifactor authentication (one time password) to verify the users logging in the system and encryption measures using bcrypt. The following are the screenshots of the codes and their outputs with explanation. 

The first step is to import the libraries like bcrypt and pyotp to support the necessary functions needed to execute the commands. The next step is to create a class in python called ‘password database’ and create functions init, register, login and bcrypt.  

 

 

 

 

The ‘init’ method creates attributes of the class password database with the parameter of self to access the attributes and instances of the class. The second function is to define the registration process with the parameters of self, user and password. The third function defines the login details with the same parameters as of register function. The fourth function is to hash the password with the initial conversion of string password to bytes then generating a general salt and passing the parameters in the ‘bcrypt.hashpw’.   

The third step is to declare object ‘password database’ with printing the process of registration and passing the dummy values in the database register. Once the values are incorporated in the database register then login process would begin by asking the username and password from the user. If the users are genuine then access to the next step would be provided. 

 

 

 

 

 

 

 

 

 

 

The final step is to implement multifactor authentication (one time password) which runs by importing PYOTP library which generates a one-time password which will be sent to the user’s phone or email address which the user would enter to gain access to the patient’s portal. 

 

In conclusion, both bcrypt and OTP allows secure user login as the encryption data stores crucial information such as password in hash values hence difficult to decrypt as well the one-time password allows an additional step in securing the users accounts from unauthorized access. 

 

 

 

 

 

 

 

 

 

 

 

If the login details are correct, the next step is to implement one time password which the user can either get through text or email. With this final step, the user will be able to access the appointment system. 

 

 

 