# Class 12 

## Accessing Data with JPA

- Start by creating a repository interface that extends one of the Spring Data JPA repository interfaces, such as CrudRepository, PagingAndSortingRepository, or JpaRepository.

- Define a method in the repository interface with a name that follows a specific naming convention. The method name should start with a keyword like findBy, getBy, readBy, queryBy, or countBy, followed by the entity attribute you want to use for filtering, and optionally, any additional query keywords like And, Or, In, OrderBy, etc.

Spring Data JPA will automatically generate the SQL or JPQL query based on the method name and the provided parameters. You don't need to write the query explicitly.

Here's an example:
package com.example.accessingdatajpa;

import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;

@Entity
public class Customer {

  @Id
  @GeneratedValue(strategy=GenerationType.AUTO)
  private Long id;
  private String firstName;
  private String lastName;

  protected Customer() {}

  public Customer(String firstName, String lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
  }

  @Override
  public String toString() {
    return String.format(
        "Customer[id=%d, firstName='%s', lastName='%s']",
        id, firstName, lastName);
  }

  public Long getId() {
    return id;
  }

  public String getFirstName() {
    return firstName;
  }

  public String getLastName() {
    return lastName;
  }
}

In this example, you store Customer objects, each annotated as a JPA entity. The following listing shows the Customer class (in src/main/java/com/example/accessingdatajpa/Customer.java)
Here you have a Customer class with three attributes: id, firstName, and lastName. You also have two constructors. The default constructor exists only for the sake of JPA. You do not use it directly, so it is designated as protected. The other constructor is the one you use to create instances of Customer to be saved to the database.

The Customer class is annotated with @Entity, indicating that it is a JPA entity. (Because no @Table annotation exists, it is assumed that this entity is mapped to a table named Customer.)

The Customer object’s id property is annotated with @Id so that JPA recognizes it as the object’s ID. The id property is also annotated with @GeneratedValue to indicate that the ID should be generated automatically.

The other two properties, firstName and lastName, are left unannotated. It is assumed that they are mapped to columns that share the same names as the properties themselves.

The convenient toString() method print outs the customer’s properties.


## Comparing repositories

- Among the Spring Data Repositories covered in the readings, the JpaRepository typically has the most methods available to it. JpaRepository extends PagingAndSortingRepository, which in turn extends CrudRepository. This hierarchy provides a wide range of CRUD (Create, Read, Update, Delete) methods for working with entities, and JpaRepository adds additional methods for more complex querying and pagination.

- One downside of using a Spring Data Repository is that it can lead to what is known as the "repository explosion" problem. This happens when you create many specialized repositories for various entities, each with their own custom query methods. Over time, this can result in a large number of repository interfaces, potentially making your codebase more complex and harder to manage. It's essential to strike a balance between creating specific repositories for entity types and keeping the codebase maintainable.

- To define an operation to find a student based on their name in a repository named StudentRepository, which extends JpaRepository, you can follow the Spring Data JPA query method naming convention. Assuming you have a Student entity with a name attribute, you can create the query method like this:
import org.springframework.data.jpa.repository.JpaRepository;

public interface StudentRepository extends JpaRepository<Student, Long> {
    // Query method to find a student by name
    Student findByName(String name);
}
In this example, the method name findByName follows the convention, and Spring Data JPA will automatically generate the SQL or JPQL query to retrieve a student by their name without you needing to write the query manually.