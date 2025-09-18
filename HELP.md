# Spring AOP Examples

This project demonstrates **Spring AOP (Aspect-Oriented Programming)** concepts using different types of pointcuts and advices in Spring Boot.  
The main aspect file is [`StudentAspect.java`](src/main/java/spring/AOP/Aspects/StudentAspect.java).

---

## 📌 What is AOP?
Aspect-Oriented Programming (AOP) helps you separate **cross-cutting concerns** (like logging, security, transactions) from your business logic.  
In Spring, AOP is commonly used with **annotations** to run additional code **before, after, or around** method execution.

---

## ⚙️ Project Structure
- **`spring.AOP.Service.StudentService`** → Service class where we define methods.
- **`spring.AOP.Aspects.StudentAspect`** → Aspect class containing multiple AOP advices.

---

## 🔑 AOP Features Shown

### 1. `@Before` Advice with `execution`
- Run code **before specific method execution**.
- Examples:
    - For a single method:
      ```java
      @Before("execution(* spring.AOP.Service.StudentService.get_the_names_of_std())")
      ```
    - For all methods in a class:
      ```java
      @Before("execution(* spring.AOP.Service.StudentService.*(..))")
      ```

---

### 2. `@Before` with `within`
- Apply advice to **all methods of a class/package**.
  ```java
  @Before("within(spring.AOP.Service.StudentService)")
