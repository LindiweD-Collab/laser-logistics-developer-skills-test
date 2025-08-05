# Junior Software Developer Skills Test (Attempt)

**Duration:** ~60–90 minutes  
**Total Marks:** 100  
**Sections:** C#, SQL/SSRS, Android, Web, General Development

---

## Section 1: C# / .NET Basics (20 points)

### 1.1. [Multiple Choice – 5 pts]  
**Q:** What is the output of the following code?

```
int x = 5;
int y = x++;
Console.WriteLine($"{x}, {y}");
```

**Answer**:
B) 6, 5


### 1.2. [Short Answer – 5 pts]
**Q**: What is the difference between a class and a struct in C#?

**Answer**:
A class is used for objects, and a struct is kind of the same but smaller. Classes support more things like inheritance.

### 1.3. [Code – 10 pts]
**Q**: Write a method to return the sum of even numbers in an array.

**Answer**:
public int SumEven(int[] arr)
{
    int total = 0;
    for (int i = 0; i < arr.Length; i++)
    {
        if (arr[i] % 2 == 0)
        {
            total = total + arr[i];
        }
    }
    return total;
}


## Section 2: SQL / SSRS (20 points)
### 2.1. [SQL Query – 8 pts]
**Q**: Return total orders per customer

**Answer**:
assuming the `Orders` table contains:

A `CustomerID` column (to group by), and an OrderID column (to count the number of orders per customer).
```
SELECT CustomerID, COUNT(OrderID)
FROM Orders
GROUP BY CustomerID;
```


### 2.2. [Short Answer – 6 pts]
**Q**: What is the purpose of a parameter in SSRS?

**Answer**:
It helps make the report dynamic... like filtering data. I think it's used when running reports to pass values. (Learning it further)

### 2.3. [Multiple Choice – 6 pts]
**Q**: Which cannot be used as a data source in SSRS?

**Answer**:
E) Notepad .txt file



## Section 3: Android Basics (15 points)
### 3.1. [Short Answer – 5 pts]
**Q**: What is AndroidManifest.xml?

**Answer**:
It’s where Android keeps info about the app like name, permissions, and screens. Sort of like a config file.


### 3.2. [Code – Java – 10 pts]
**Q**: Display a Toast on button click

**Answer**:
```
Button b = findViewById(R.id.button);
b.setOnClickListener(new View.OnClickListener() {
    public void onClick(View v) {
        Toast.makeText(MainActivity.this, "Clicked", Toast.LENGTH_LONG).show();
    }
});
```


## Section 4: Web (20 points)
### 4.1. [HTML – 5 pts]
**Q**: Write a form with a text input and a submit button.

**Answer**:
```
<form id="myForm">
  <input type="text" name="username" placeholder="Enter your name" required />
  <button type="submit">Submit</button>
</form>
```

### 4.2. [JavaScript – 5 pts]
**Q**: Write JS code that shows an alert when the form is submitted.

**Answer**:
```
document.getElementById("myForm").addEventListener("submit", function(event) {
  event.preventDefault(); 
  alert("Form submitted!");
});
```


### 4.3. [Short Answer – 10 pts]
**Q**: Role of Controller in ASP.NET MVC?

**Answer**:
The Controller in ASP.NET MVC:

- Handles user input and interactions

- Processes incoming HTTP requests

- Works with the Model to retrieve or save data

- Selects the appropriate View to return to the user

- It acts as the coordinator between Model (data) and View (UI).


## Section 5: General Development (25 points)
### 5.1. [Short Answer – 5 pts]
**Q**: What are REST APIs and why are they useful?

**Answer**:
REST APIs (Representational State Transfer) are web services that use standard HTTP methods (GET, POST, PUT, DELETE) for communication.
They are useful because they:

Allow communication between different systems

Enable frontend and backend separation

Use standard formats like JSON or XML


### 5.2. [Short Answer – 5 pts]
**Q**: Purpose of Git in teams?

**Answer**:
Git helps teams by:

Tracking changes to code over time

Allowing multiple developers to work on the same codebase without conflicts and Facilitating collaboration through platforms like GitHub or GitLab


### 5.3. [Scenario – 10 pts]
**Q**: Steps to build SSRS report to show customer orders by date range.

**Answer**:

Open SQL Server Data Tools / Report Builder

Create a new report

Define a data source (e.g., SQL Server database)

Create a dataset with a SQL query using date parameters:

SELECT * FROM Orders
WHERE OrderDate BETWEEN @StartDate AND @EndDate
Add report parameters: @StartDate and @EndDate

Design the report layout (e.g., use tables or charts)

Bind dataset fields to the report elements

Preview and test the report with sample dates

Deploy the report to the SSRS server

Access via browser or integrate into a portal/dashboard


### 5.4. [Code Review – 5 pts]
**Q**: Review this method and suggest 2 improvements:

```
public void PrintHelloWorld() {
    string message = "Hello";
    message += " ";
    message += "World!";
    Console.WriteLine(message);
}```

**Answer**:

```
public static void PrintHelloWorld() {
    Console.WriteLine("Hello World!");
}
 ```
