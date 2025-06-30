# Spring-boot-store-project
this project is built using spring boot framework that is one of the projects built using spring framework, it simplifies spring development.
## Technologies Used
- Java
- Spring Boot
- Maven
- Spring MVC

# Key Learnings
 
## 1.how to generate a springboot project
## 2.project structure:
-pom.xml:some configurations and dependencies
-src folder(main:java(actual code) and resources)
## 3.Dependencies:
### learned how to add a dependency;
-through downloading it from maven central the copying the code into pom.xml then reloading the project
-or we can download it directly in intellij

## 4.Controller
### Spring MVC (how springboot handles web requests)
#### Model: related to data
#### View: what the user sees
#### Controller:handles requests, interacts with the model, tells the view what to display

### learned how to create a controller:
1.create a java class.
2.put this annotation :
```
@Controller
public class HomeController {
   }
```
3.add methods so that when the user send a request these methods are called.to apply:(between "" URL pattern)
```
@RequestMapping("")
public String index() {
}
```
4.if a view should be returned then the ruturn statement should have the vieww name that must be created in the resources.

## 5.Dpemdency Injection
### Dpendency
some classes(A) are dependent on other classes(B), so when we want to change class B A must be modified also, and this causes problems.
### to solve this:
we create an interface and classes(B) that implement this interface. In this way class A depends on the interface.
### Dependency Injection
#### 1.via Constructor injection:(recpmmended)
pass an object of the interface to the constructor of class A
example:
```
public OrderService(PaymentService paymentService){this.paymentService=paymentService}
```
and in the main method when passing the object to the constructor create it from the class that implements the interface.(dependency injection)
example:
```
var OrderService= new OrderService(new StripePaymentService());
```
#### 2.via setter injection:
declare a variable of the interface type and a setter for it
in the main method call the setter method and pass the object of the class that implements the interface.







