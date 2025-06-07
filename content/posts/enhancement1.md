+++
date = '2025-06-06T03:42:43-05:00'
draft = true
title = 'Software Engineering Enhancement'
weight = 2
featured_image = "/images/rainbow.jpg"
+++
### C# Graphical User Interface Implementation



<!--more-->


&nbsp;&nbsp;&nbsp;&nbsp;This enhancement artifact, developed in CS 410 Software Reverse Engineering, is a console application that was reverse-engineered and translated into C++ source code earlier this year (2025). Designed for an investment company, the application managed five client accounts, each classified as either retirement or brokerage, using a single, hardcoded password embedded in the binary. Upon launch, the application required authentication and terminated if given an incorrect password. Once authenticated, a menu allowed users to list accounts, change investment options, or exit the program. 

&nbsp;&nbsp;&nbsp;&nbsp;Chosen for enhancement, this artifact possessed significant potential for improvement, making it an excellent candidate for the software design and engineering category. The original application, limited to only five hardcoded accounts and a single administrator, lacked compelling features, such as adding or removing users or accounts, data persistence after-program closure, and encryption. Additionally, converting the console-based application into a graphical user interface (GUI) made the application more appealing and accessible to modern users. 

&nbsp;&nbsp;&nbsp;&nbsp;The enhancement process demonstrated several software development skills by translating into a new programming language and application type and requiring the deconstruction of the application’s functionality. The console application was transformed into a C# Windows Presentation Foundation (WPF) desktop application, replacing the original console menu with visual window elements. Additionally, functionality was translated and improved. For example, user authentication previously reliant on only a hardcoded password now required both a username and password for stronger security. The password, hashed through the SHA-256 (Secure Hash Algorithm 256-bit) algorithm and encrypted with AES (Advanced Encryption Standard), is saved to the hard disk for persistence.

&nbsp;&nbsp;&nbsp;&nbsp;Similarly, account management was enhanced by replacing the five hardcoded accounts with the ability to create, delete, and modify accounts, which are also encrypted and saved to the disk for persistence. Furthermore, the application was restructured from a single-script artifact into the Model-View-ViewModel (MVVM) architecture, commonly used in WPF applications. This architecture separates concerns among the view (user interface), the view model (intermediary), and the model (business logic), facilitating easier development, testing, and maintenance. 

&nbsp;&nbsp;&nbsp;&nbsp;In summary, the enhancements improved user experience, security, persistence, and functionality. The goal of this project was to meet the course outcome: “Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices to implement computer solutions that deliver value and accomplish industry-specific goals (software engineering/design/database).” This was achieved through several key improvements aligned with industry standards and modern software engineering practices: 


- Transitioning from a console-based application to a C# WPF application with a GUI showcased the use of tools like XAML (Extensible Application Markup Language) to enhance user experience and meet contemporary expectations. Adopting the MVVM architecture further demonstrated sound software design principles, promoting maintainability, testability, and scalability through the separation of concerns. 

- Implementing advanced security measures, such as SHA-256 password hashing and AES encryption, addressed the need for securing data at rest. These enhancements ensure the protection of sensitive data, including authentication credentials and account information, thus aligning with industry standards for secure software solutions. 

- Adding data persistence through disk storage and enabling the creation, deletion, and modification of accounts significantly increased the application’s value. 


&nbsp;&nbsp;&nbsp;&nbsp;These features transformed the original artifact from a limited program with hardcoded accounts into a dynamic, user-friendly system capable of meeting real-world investment company requirements. This demonstrated the ability to design and implement a database-like solution supporting flexible and persistent account management. Overall, the enhancements improved usability and functionality while directly addressing the course outcome by leveraging industry-standard tools, innovative techniques, and skills to deliver a valuable solution. 

&nbsp;&nbsp;&nbsp;&nbsp;The enhancement process was more complex than initially anticipated. Rather than a simple translation of the program from C++ to C#, the application underwent a fundamental transformation. Unlike a console application that runs sequentially in a loop, the enhanced application creates hundreds of objects and employs callbacks, data binding, and other mechanisms to connect use cases while maintaining a responsive user interface. 

&nbsp;&nbsp;&nbsp;&nbsp;Unforeseen challenges arose during development, including encryption issues, input validation, and missing properties. For instance, a new property, IsAdmin, had to be added to the user model to restrict account addition and removal to a single administrative account. Input validation to enforce unique usernames was overlooked initially and had to be added later. The most challenging aspect was serializing two data structures, a list of accounts, and a list of users, into a single string for storage. Key lessons learned included working with declarative markup languages for the views, implementing data binding and events in the view models, and mastering encryption and serialization in the models.



See the original artifact here [CS410 Artifact](https://github.com/mufg80/CS_410_ReverseEngineering)

See the enhancement here [CS410 Enhancement](https://github.com/mufg80/CS410_Enhancement_InvestmentAccounts)

## **Code Review**

{{< youtube pZR-EUxrckI >}}


