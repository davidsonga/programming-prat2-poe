[david_sonag_st10081790_progPart2.zip](https://github.com/davidsonga/programming-prat2-poe/files/11588964/david_sonag_st10081790_progPart2.zip)
default employee login 
username: employee
password: 0000

default farmer login details
username: david
password: 0000

username: daniel
password  1234

username: celine
password: 1111


username: songa
password: 2222


this program uses azure sql database with 2 table that are LoginDetails and productDetails.
1. in LoginDetails that is where all authentication takes place, when a employee/farmer is register we save his/her details by giving he/she a unique number so that whenenver he / she add a product that unique that will be add on that product to allow us to know who added it.
2. productDetails is where the farmer product are saved using the unique iD number their got when they signed up that unique number allows us to easily know who does this product belows too.




the program consiste of 5 razor pages 
1. index is the login page
2. EmployeeMenu is use to disply a table and filter that an employee can use on the farmer products
3. Register is the employee can register a new farmer or new employee by giving them a user name and password
4. FarmerProduct it help the farmer to insert new product into our azure that database 
5. FarmerProductMenu is a menu that display to the farmer all the add product

every razor pages has it owm cshtml, cs and i created the css file in css folder.

why css?

to give a beautiful appearance to each pages.


this application contain 3 folders where the main code are kept they are;
1 SQL Connection folder: this folder holds connectionString.cs this class is functionality is to connect/disconnect our application to azure sql connection 
2 SQL querries folder : this folder holds two class they are:
A1. sqlReadquerry.cs: this class is used to retrieve data from our azure sql depending on the querries we ask from the class
A.2 sqlWriteQuerry.cs: this class is used to insert data into our Azure sql database depending on the querry we ask the class do to for us.
3. util folder: this folder holds 3 classes they are;
A1. farmerProducts.cs: this class it is used as an object class to a list called in sqlReadquerry.cs and sqlWriteQuerry.cs to retrieve or save the farmer username and id
A.2 IOWriteRead.cs: this class uses file writer to write the id and name of our farmer so we he can save accordingly to the is unique id without the application giving null values
A.3OnlineStorage.cs: this class it is used as an object class to a list called in sqlReadquerry.cs and sqlWriteQuerry.cs to retrieve or save id,farmer name, product, location, quntity, and price.
