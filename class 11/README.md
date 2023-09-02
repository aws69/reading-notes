## Spring Boot 

Spring Boot helps you to create Spring-powered, production-grade applications and services with absolute minimum fuss. It takes an opinionated view of the Spring platform so that new and existing users can quickly get to the bits they need.

You can use Spring Boot to create stand-alone Java applications that can be started using java -jar or more traditional WAR deployments. We also provide a command-line tool that runs Spring scripts.

## Spring App Basics

### @Controller in a Spring MVC application

In Spring’s approach to building web sites, HTTP requests are handled by a controller. You can easily identify the controller by the @Controller annotation. In the following example, GreetingController handles GET requests for /greeting by returning the name of a View (in this case, greeting). A View is responsible for rendering the HTML content. The following listing (from src/main/java/com/example/servingwebcontent/GreetingController.java) shows the controller:
package com.example.servingwebcontent;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class GreetingController {

	@GetMapping("/greeting")
	public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {
		model.addAttribute("name", name);
		return "greeting";
	}

}

This controller is concise and simple, but there is plenty going on. We break it down step by step.

The @GetMapping annotation ensures that HTTP GET requests to /greeting are mapped to the greeting() method.

@RequestParam binds the value of the query string parameter name into the name parameter of the greeting() method. This query string parameter is not required. If it is absent in the request, the defaultValue of World is used. The value of the name parameter is added to a Model object, ultimately making it accessible to the view template.

The implementation of the method body relies on a view technology (in this case, Thymeleaf) to perform server-side rendering of the HTML. Thymeleaf parses the greeting.html template and evaluates the th:text expression to render the value of the ${name} parameter that was set in the controller.The following listing (from src/main/resources/templates/greeting.html) shows the greeting.html template:
<!DOCTYPE HTML>
<html xmlns:th="http://www.thymeleaf.org">
<head> 
    <title>Getting Started: Serving Web Content</title> 
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
</head>
<body>
    <p th:text="'Hello, ' + ${name} + '!'" />
</body>
</html>


### GET request

Think of a GET request as a friendly way of asking for information on the internet. Imagine you're browsing a library catalog. When you type a book's title into the search bar and hit enter, your computer sends a GET request to the library's website. It's like saying, "Hey, can you give me information about this book?"

The website then responds by showing you the book's details, like its title, author, and availability. In this case, the GET request is like a question, and the website's response is the answer.

### Annotation for a Spring Boot application class

 In a Spring Boot application, you'll often see an annotation called @SpringBootApplication on the main application class. Think of this annotation as the starting point of your application, like the grand opening of a new store.

When you see this annotation, it tells the computer that this class is where everything begins. It's like putting a big sign on your bakery that says, "This is where we start making and selling delicious cakes!" This annotation helps Spring Boot set up your application correctly and makes it ready to serve your customers (users) over the internet.

## Spring MVC and Thymeleaf

### Displaying a Java variable in HTML with Thymeleaf
To display a Java variable in HTML using Thymeleaf in a Spring Controller, you typically use a Thymeleaf attribute called th:each or th:text.

th:each is used when you have a collection of objects (like a list) and you want to iterate through them to display each item. It's like having a menu at your bakery, and you use th:each to list all the available cake flavors.
th:text is used when you want to display a single variable or value. Imagine you want to display the price of a cake, you'd use th:text to show that price in the HTML.
For example: 
<tr th:each="message : ${messages}">
        <td th:text="${message.id}">1</td>
        <td><a href="#" th:text="${message.title}">Title ...</a></td>
        <td th:text="${message.text}">Text ...</td>
    </tr>

Here, th:each is used to iterate messages collection in your HTML.
And, th:text is used to insert the value of the message.id, message.title, and message.text variable into the collection in your HTML.

### Role of a @Controller class in a Spring MVC application

In a typical Spring MVC application, @Controller classes are responsible for preparing a model map with data and selecting a view to be rendered. This model map allows for the complete abstraction of the view technology and, in the case of Thymeleaf, it is transformed into a Thymeleaf context object (part of the Thymeleaf template execution context) that makes all the defined variables available to expressions executed in templates.

### Model attribute referred to in Thymeleaf

Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables.

There are several ways of adding model attributes to a view in Spring MVC. Below you will find some common cases:

Add attribute to Model via its addAttribute method:

    @RequestMapping(value = "message", method = RequestMethod.GET)
    public String messages(Model model) {
        model.addAttribute("messages", messageRepository.findAll());
        return "message/list";
    }
Return ModelAndView with model attributes included:

    @RequestMapping(value = "message", method = RequestMethod.GET)
    public ModelAndView messages() {
        ModelAndView mav = new ModelAndView("message/list");
        mav.addObject("messages", messageRepository.findAll());
        return mav;
    }
Expose common attributes via methods annotated with @ModelAttribute:

    @ModelAttribute("messages")
    public List<Message> messages() {
        return messageRepository.findAll();
    }
As you may have noticed, in all the above cases the messages attribute is added to the model and it will be available in Thymeleaf views.

In Thymeleaf, these model attributes (or context variables in Thymeleaf jargon) can be accessed with the following syntax: ${attributeName}, where attributeName in our case is messages. This is a Spring EL expression. In short, Spring EL (Spring Expression Language) is a language that supports querying and manipulating an object graph at runtime.

You can access model attributes in views with Thymeleaf as follows:

    <tr th:each="message : ${messages}">
        <td th:text="${message.id}">1</td>
        <td><a href="#" th:text="${message.title}">Title ...</a></td>
        <td th:text="${message.text}">Text ...</td>
    </tr>