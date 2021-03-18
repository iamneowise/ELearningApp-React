![](https://bn1305files.storage.live.com/y4mzAYxmbIIC_nmvccsxcMxIn078c3vVvo2hjmltqaoRhEtWlZnI3JdbZUICY8PZjRjDjzi6d47a7zaC2NaTN9AaLfskm8L0JfZYbvlVV9x9FK4MITpOUlH2De2JA_E0Cx8wETaL1rGxOma5KhqurIUC9RHIZDz5CTBIExxgZ37CNy0EUsamWWWsrg03qQy3hRe?width=369&height=137&cropmode=none)
# iamneo | Ecommerce | E-Learning | React-Springboot-Fullstack-App


**Objective:**

E-Learning resource is an online application to be built education based website/software , helping students to get all resources & study materials of every courses available. It uses “E-Book” facility. It is reliable & time efficient approach compared to all links of the website provided by any search engine while searching for course materials.

**Users of the System:**

1.	Admin
2.	Professors
3.	Users

**Functional Requirements:**

- To provide official & legal links of the website from which user(student ) can download resources & study materials of relevant course.
-	Only accessible after registering to that specific website.
-	Getting associated with professors of esteemed institutes & colleges.
-	To provide interaction between professor & students.
-	Not all links provided by GOOGLE are virus free or recommended to download. This would be a better approach.

**Output/ Post Condition:**

	Records Persisted in Success & Failure Collections
	Standalone application / Deployed in an app Container

---

# Non-Functional Requirements:

| **Security** |
- App Platform –UserName/Password-Based Credentials
- Sensitive data has to be categorized and stored in a secure manner
- Secure connection for transmission of any data
 ***
| **Performance** |
- Peak Load Performance (during Festival days, National holidays etc)
- eCommerce -\&lt; 3 Sec
- Admin application \&lt; 2 Sec
- Non Peak Load Performance
- eCommerce \&lt; 2 Sec
- Admin Application \&lt; 2 Sec
***
| **Availability** |
- 99.99 % Availability
***
| **Standard Features** |
- Scalability
- Maintainability
- Usability
- Availability
- Failover
 ***
| **Logging &amp; Auditing** |
- The system should support logging(app/web/DB) &amp; auditing at all levels
 ***
| **Monitoring** |
- Should be able to monitor via as-is enterprise monitoring tools
***
| **Cloud** |
- The Solution should be made Cloud-ready and should have a minimum impact when moving away to Cloud infrastructure
 ***
| **Browser Compatible** |
- IE 7+
- Mozilla Firefox Latest – 15
- Google Chrome Latest – 20
- Mobile Ready
 ***

|               | Technology Stack                                                                 |                          |   |   |
|---------------|----------------------------------------------------------------------------------|--------------------------|---|---|
| Frontend      | React 16+                                                                        | Bootstrap or Bulma       |   |   |
| Server Side   | Spring BootSpring Web (Rest Controller)Spring SecuritySpring AOPSpring Hibernate |                          |   |   |
| Core Platform | OpenJDK 11                                                                       |                          |   |   |
| Database      | MySQL or H2                                                                      |                          |   |   |

---
| **Platform Pre-requisites (Do&#39;s and Don&#39;ts):** |

1. The angular app should run in port 8081. Do not run the angular app in the port: 4200.
2. Spring boot app should run in port 8080.
---
**Key points to remember:**

1. The id (for frontend) and attributes(backend) mentioned in the SRS should not be modified at any cost. Failing to do may fail test cases.
2. Remember to check the screenshots provided with the SRS. Strictly adhere to id mapping and attribute mapping. Failing to do may fail test cases.
3. Strictly adhere to the proper project scaffolding (Folder structure), coding conventions, method definitions and return types.
4. Adhere strictly to the endpoints given below.

**Application assumptions:**

1. The login page should be the first page rendered when the application loads.
2. Manual routing should be restricted by using AuthGaurd by implementing the canActivate interface. For example, if the user enters as [http://localhost:4200/signup](http://localhost:4200/signup) or [http://localhost:4200/home](http://localhost:4200/home) the page should not navigate to the corresponding page instead it should redirect to the login page.
3. Unless logged into the system, the user cannot navigate to any other pages.
4. Logging out must again redirect to the login page.
5. To navigate to the admin side, you can store a user type as admin in the database with a username and password as admin.
6. Use admin/admin as the username and password to navigate to the admin dashboard.

**Validations:**

1. Basic email validation should be performed.
2. Basic mobile validation should be performed.

**Project Folder Structure : (Component Structure)**
![](https://bn1305files.storage.live.com/y4mePqHvD5ntYT71LXJ_jSuMfTbceiHilr0INDRYace2TsRmiQyhhapSqVXMTC1o9KqdeXtY7DSl7eLqfGpEfmk1PnkzXwROlM3lkahonPPOeRi3ihHZL_1gRpW5GWntQHM3nLZWxOJWm0w0R6q9z9RE4hz6EBsLoVC_DUkS_vHn_Bcs_mxZjMiF3SJThAW7aQI?width=728&height=516&cropmode=none)
---

## Project Tasks:

**API Endpoints:**

| **USER** |

| Action           | URL        | Method | Response           |
|------------------|------------|--------|--------------------|
| Login            | /login     | POST   | true/false         |
| Signup           | /signup    | POST   | true/false         |
| Get All Resource | /home      | GET    | Array of Resource  |
| Update Resource  | /home/{id} | PUT    | Updated Success    |
| Add Resourse     | /home      | POST   | Added Successfully |
| Delete Resource  | /home/{id} | DELETE | Resource Deleted   |
| Start Chat       | /chat/{id} | POST   | Chat Started       |
| Get Chat         | /chat/{id} | GET    | Array of Chat      |
| Delete Chat      | /chat/{id} | DELETE | Chat Deleted       |

| **ADMIN** |

| Action          | URL                  | Method | Response        |
|-----------------|----------------------|--------|-----------------|
| Get All User    | /admin               | GET    | Array of Users  |
| Approve User    | /admin/verify        | POST   | User Verified   |
| Delete User     | /admin/delete/{id}   | DELETE | User deleted    |
| Update Resource | /admin/resourse/{id} | PUT    | Updated Success |

---
## Frontend

**Customer:**
```
Signup: Design a signup page component where the new customer has options to sign up by providing their basic details.
  1. Ids:
    1. email
    2. username
    3. mobilenumber
    4. password
    5. confirmpassword
  2. API endpoint Url: [http://localhost:4200/signup](http://localhost:4200/signup)
  3. Output screenshot:
```
![]()

```
Login: Design a login page component where the existing customer can log in using the registered email id and password.
  1. Ids:
    1. email
    2. password
  2. API endpoint Url: [http://localhost:4200/login](http://localhost:4200/login)
  3. Output screenshot:
```
![]()

```
Dashboard / Home: Design a home page component that has the navigation bar and lists all the available products as grid elements with appropriate filter options.
  1. Ids:
    1. homeButton
    2. cartButton
    3. orderButton
  2. API endpoint Url: [http://localhost:4200/](http://localhost:4200/login)home
  3. Screenshot
```
![]()

```
Cart and Orders: Design a cart component and order component where we can see the cart items and see the items ordered after placing an order.
  1. Ids
    1. cartBody
    2. orderBody
  2. API endpoint Url: [http://localhost:4200/](http://localhost:4200/login)cart
  3. API endpoint Url: [http://localhost:4200/orders](http://localhost:4200/orders)
  4. Screenshot
```
![]()

**Admin:**

```
Admin Dashboard: Design a dashboard page where the list of products is displayed on the admin side.
  1. Ids
    1. addProduct
    2. productBody
  2. API endpoint Url: [http://localhost:4200/admin](http://localhost:4200/admin)
  3. Screenshot
```
![]()

```
Admin Navigation: Design a navigation component that can navigate to products and orders.
  1. Ids:
    1. adminOrderButton
    2. productButton
    3. logoutButton
  2. Screenshot:
```
![]()

```
Add Product: Design an add product component in which the admin can add new products to the inventory.
  1. Ids:
    1. addProductBody
    2. productName
    3. productPrice
    4. description
    5. imageURL
    6. quantity
    7. addProductButton
  2. API endpoint Url: [http://localhost:4200/ad](http://localhost:4200/ad)dProduct
  3. Screenshot
```
![]()

```
View Orders: Create a view component where the admin can look into the new and old orders.
  1. Ids:
    1. adminOrderBody
  2. API endpoint Url: [http://localhost:4200/admin](http://localhost:4200/admin)/orders
  3. Screenshot
```
![]()

## Backend

**Class and Method description:**

**Model Layer:**
```
1. EmployeesModel: This class stores the details of the Employees information.
  1. Attributes:
    1. username: String
    2. password: String
    3. email: String
    4. mobileNumber: Long
    5. vehicleModel: String
    6. vehicleNumber: String
    7. verified: Boolean
    8. active: Boolean
  2. Methods: -
2. LoginModel: This class contains the email and password of the user.
  1. Attributes:
    1. email: String
    2. password: String
  2. Methods: -
3. CustomerModel: This class stores the details of the Corporate Employees.
  1. Attributes:
    1. customerId: String
    2. customerName: String
    3. emailId: String
    4. mobileNumber: Long
    5. status: Boolean
  2. Methods: -
4. RouteModel: This class stores the route details.
  1. Attributes:
    1. routeId: int
    2. startPoint: String
    3. endPoint: String
    4. distance: int
  2. Methods: -

```

**Controller Layer:**
```
1. SignupController: This class control the user signup
  1. Attributes: -
  2. Methods:
    1. saveCustomer(CustomerModel user): This method helps to store Customer in the database and return true or false based on the database transaction.
2. LoginController: This class controls the user login.
  1. Attributes: -
  2. Methods:
    1. checkUser(LoginModeldata): This method helps the user to sign up for the application and must return true or false
3. EmployeeController: This class controls the add/edit/update/view Employees.
  1. Attributes: -
  2. Methods:
    1. List<EmployeModel>getEmployee(): This method helps the admin to fetch all employees from the database.
    2. EmployeModel getEmployeeById(Stringid): This method helps to retrieve a Employee from the database based on the employee id.
    3. EmployeeModel editEmployee(EmployeeModeldata): This method helps to edit a employee and save it to the database.
    4. saveEmployee(EmployeeModeldata): This method helps to add a new employee to the database.
    5. deleteEmployee(Stringid): This method helps to delete a Employee from the database.
4. RouteController: This class helps in add, delete, update, delete the Route.
  1. Attributes: -
  2. Methods:
    1. List<RouteModel> getRoute(): This method helps the Customer to fetch all route from the database.
    2. RouteModel getRouteById(String id): This method helps to retrieve a Route from the database based on the route id.
    3. RouteModel editRoute(RouteModel data): This method helps to edit a route and save it to the database.
    4. saveRoute(RouteModel data): This method helps to add a new Route to the database.
    5. deleteRoute(String id): This method helps to delete a Route from the database.
5. BookingController: This class helps to booking the car.
  1. Attributes: -
  2. Methods:
    1. List<BookingModel> getBooking (): This method helps the admin to fetch all booking from the database.
    2. BookingModel getBookingById(String id): This method helps to retrieve a Booking from the database based on the userId.
    3. saveBooking(BookingModel): This method helps the customer to add a new Bookingto the database.
 ```
## Application Workflow

Admin Flow (Click to see the output)
> <>

User Flow (Click to see the output)
> <>

Happy Coding Neos👍
