EXPLANATION:BACK-END
1. Install Visual Studio 2022
Make sure you have Visual Studio 2022 installed on your machine. You can download it from the official Visual Studio website.

2.Create a New ASP.NET Core Web API Project
     1.Open Visual Studio 2022.
     2.Go to "File" > "New" > "Project...".
     3.In the "Create a new project" dialog, search for "ASP.NET Core Web API".
     4.Select "ASP.NET Core Web API" template and click "Next".
     5.Configure your new project (e.g., choose a name and location) and click "Create".

3.Then just build the solution once

4.Right click on the dependencies then select the Manage NuGet Package

5.Then install the Microsoft.EntityFrameworkCore.Tools

6.And install the  Microsoft.EntityFrameworkCore.SqlServer

7.After that build the solution

8.In Tools,select the NuGet Package Manager nd select the Package Manager Console

9.Give the commnds with respect to the sql server nd database

10.after that select the controller with respect to the model

11.Select the controller 

12.In the APP SETTING JSON,give the connection string


"ConnectionStrings": {
    "ListDbContext": "server=DESKTOP-JPNMO15;database=ToDoAppDb;trusted_connection=true; TrustServerCertificate=true;"
  }


13.In the Program.cs:We are enabling the cors


builder.Services.AddDbContext<ListDbContext>(options =>
   options.UseSqlServer(builder.Configuration.GetConnectionString("ListDbContext")));

var app = builder.Build();
app.UseCors(Options => Options.WithOrigins("http://localhost:4200").AllowAnyMethod().AllowAnyHeader());


14.Build the solution and Run the programme

15.We can get the output.

16.After that you can check through the swagger nd GET PUT POST DELETE 

17.The HTTP methods GET, PUT, POST, and DELETE are used to perform different operations. These methods correspond to the CRUD (Create, Read, Update, Delete) operations commonly associated with database applications and RESTful APIs


1.GET: This method is used to retrieve information or data from the server. When you make a GET request to a specific endpoint (URL), you are asking the server to give you some data.

2.PUT: This method is used to update or create a resource on the server. When you make a PUT request to a specific endpoint, you are either updating the existing resource if it already exists, or creating a new one if it doesn't.

3.POST: This method is used to submit data to be processed to a specified resource. It is often used to create a new resource on the server. When you make a POST request, you are sending data to the server for it to process.

4.DELETE: This method is used to request that a resource be removed or deleted. When you make a DELETE request to a specific endpoint, you are asking the server to delete the resource associated with that endpoint.

In simple Terms,
   
GET is like asking for information.
PUT is like updating or creating something.
POST is like submitting data to be processed.
DELETE is like asking to remove something.

These methods help define the actions that can be performed on the server, allowing clients (such as a web or mobile application) to interact with the data stored on the server.

ANGULAR:

 Angular is a front-end application we have already created the folder front end inside the folder open the command prompt and type the commands.

1.Installing Angular CLI

npm install -g @angular/cli

2.After that create the new Project of Angular running by the following command

ng new frond-end

3.Select the SCSS Style for the Advanced CSS and Press Enter Key.

After complete the installation then run the project using following command.

ng serve

4.
it will generate the url link to run the angular application.paste the url in to the browser

5.Now you see the Angular Welcome Page.

After that open the Angular project into VS code editor.

now you can see the following file structure

6.Creating a new Component 

ng g c customer

7.After that install the Bootstrap by typing the following command

npm i bootstrap

8.Handle User Input means add the HTML template to display input fields and a button.

9. Integrate Component in App means include the <app-(give the componnet name)> component.

10. Run the Application

     1.Save your changes and run the application: ng serve --open
     2.Open your browser and navigate to http://localhost:4200/.
     3.This example is a simple demonstration of creating an Angular project

Testing:

1. Create a Test Project
    
    Create a new test projectin the vs 2022

2.After that add the TodoApp.dll 

3.Install Nunit,Moq And Nunit Test Adapter by cliking on the Nuget Package Manager

4.Build the solution once

5. Write Test Methods
Create a test class and write test methods to verify the behavior of the Student class.
6.Use the Arrange, Act, Assert (AAA) pattern in your test methods.
Write test methods that cover different scenarios, such as setting properties, handling edge cases, etc.
Consider using parameterized tests to test different inputs and expected outputs in a single test method.

7.Step 4: Run Tests
Save your test project and the test class.
Open the Test Explorer window (View > Test Explorer or use the keyboard shortcut Ctrl+E, T).
In the Test Explorer window, you should see your test methods listed.
Right-click on the test class or individual test methods and select "Run Tests" or use the keyboard shortcut Ctrl+R, A.
The Test Explorer will show the results of your tests. Green checkmarks indicate passing tests, and red crosses indicate failing tests.

finally
      FRONT-END WE USED THE ANGULAR.
      BACKEND WE USED THE REST API.
      SERVERSIDE WE USED THE SQL SERVER.
      TESTING WE USEd THED NUNIT.

OOPS PRICIPLES:

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data in the form of fields (often known as attributes or properties) and code, in the form of procedures (often known as methods). The four main principles of OOP are encapsulation, inheritance, polymorphism, and abstraction.

1.Encapsulation:
Simple Explanation: Encapsulation is like putting things in a box. You have some data (variables) and the methods (functions) that work on that data, and you put them together in a class.
Example: Think of a TV remote. You don't need to know how the buttons inside the remote work; you just press the buttons, and the remote does its job. The internal workings are encapsulated within the remote.

2.Inheritance:
Simple Explanation: Inheritance is like inheriting traits from your parents. A new class (child class) can use the properties and methods of an existing class (parent class).
Example: If you have a class representing a generic "Vehicle," you can create a more specific class like "Car" or "Motorcycle" that inherits characteristics from the "Vehicle" class.

3.Polymorphism:
Simple Explanation: Polymorphism is like using the same name for different things. You can use a single interface (method name) to represent different implementations.
Example: Think of a "draw" method. In a "Circle" class, it might draw a circle, and in a "Square" class, it might draw a square. You use the same method name ("draw"), but the actual behavior depends on the object.

4.Abstraction:
Simple Explanation: Abstraction is like simplifying things by showing only what's necessary. You focus on the essential features and ignore unnecessary details.
Example: When you drive a car, you don't need to know how the engine works. 

DRY PRICIPLE:

The DRY principle, which stands for Don't Repeat Yourself, is a fundamental best practice in software development. Its core message is simple: every piece of knowledge should have a single, unambiguous, authoritative representation within a system. In other words, you should avoid duplicating code or logic wherever possible.
By adhering to the DRY principle, you can achieve numerous benefits for your software:
Reduced code size: Eliminating duplicate code reduces the overall size of your codebase, making it easier to navigate and maintain.
Increased maintainability: When code is centralized and not duplicated, it becomes much easier to modify and update in the future. Changes only need to be made in one place, instead of multiple locations.
Reduced risk of errors: Duplicate code can easily become inconsistent and lead to subtle errors. Following the DRY principle helps to ensure that your code is consistent and reliable.
Improved performance: Duplicate code can often lead to inefficient performance. Eliminating redundancy can help to improve the overall performance of your software.



