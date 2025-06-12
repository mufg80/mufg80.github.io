+++
date = '2025-06-06T03:42:43-05:00'
draft = false
title = 'Software Engineering Enhancement'
weight = 2
featured_image = "/images/enhancement1.png"
cover_dimming_class = "bg-white-10"
omit_header_text = true
+++
### C# Graphical User Interface Implementation

<!--more-->

&nbsp;&nbsp;&nbsp;&nbsp;This enhancement artifact, developed in CS 410 Software Reverse Engineering, is a console application that was reverse-engineered and translated into C++ source code earlier this year (2025). Designed for an investment company, the application managed five client accounts, each classified as either retirement or brokerage, using a single, hardcoded password embedded in the binary. Upon launch, the application required authentication and terminated if given an incorrect password. Once authenticated, a menu allowed users to list accounts, change investment options, or exit the program. 

&nbsp;&nbsp;&nbsp;&nbsp;Chosen for enhancement, this artifact possessed significant potential for improvement, making it an excellent candidate for the software design and engineering category. The original application, limited to only five hardcoded accounts and a single administrator, lacked compelling features, such as adding or removing users or accounts, data persistence after-program closure, and encryption. Additionally, converting the console-based application into a graphical user interface (GUI) made the application more appealing and accessible to modern users. 

&nbsp;&nbsp;&nbsp;&nbsp;The enhancement process demonstrated several software development skills by translating it into a new programming language and application type and requiring the application’s functionality to be reapplied in a GUI. The console application was transformed into a C# Windows Presentation Foundation (WPF) desktop application, replacing the original console menu with an event driven visual element. Additionally, functionality was improved, for example, user authentication previously reliant on only a hardcoded password now required both a username and password for stronger security. The password, hashed through the Secure Hash Algorithm 256-bit(SHA-256) algorithm and encrypted with the Advanced Encryption Standard (AES), is saved to the hard disk for persistence.

&nbsp;&nbsp;&nbsp;&nbsp;Similarly, account management was enhanced by replacing the five hardcoded accounts with the ability to create, delete, and modify accounts, which are also encrypted and saved to the disk for persistence. Furthermore, the application was restructured from a single-script artifact into the Model-View-ViewModel (MVVM) architecture, commonly used in WPF applications. This architecture separates concerns among the view (user interface), the view model (intermediary), and the model (business logic), facilitating easier development, testing, and maintenance. 

&nbsp;&nbsp;&nbsp;&nbsp;In summary, the enhancements improved user experience, security, persistence, and functionality. The goal of this project was to meet the course outcome: “Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices to implement computer solutions that deliver value and accomplish industry-specific goals.” This was achieved through several key improvements aligned with industry standards and modern software engineering practices: 

- Transitioning from a console-based application to a C# WPF application with a GUI showcased the use of tools like XAML (Extensible Application Markup Language) to enhance user experience and meet contemporary expectations. 

- Adopting the MVVM architecture further demonstrated sound software design principles, promoting maintainability, testability, and scalability through the separation of concerns. 

- Implementing advanced security measures, such as SHA-256 password hashing and AES encryption, addressed the need for securing data at rest. These enhancements ensure the protection of sensitive data, including authentication credentials and account information, thus aligning with industry standards for secure software solutions. 

- Adding data persistence through disk storage and enabling the creation, deletion, and modification of accounts significantly increased the application’s value. 

&nbsp;&nbsp;&nbsp;&nbsp;These features transformed the original artifact from a limited program with hardcoded accounts into a dynamic, user-friendly system capable of meeting real-world investment company requirements. This demonstrated the ability to design and implement a database-like solution supporting flexible and persistent account management. Overall, the enhancements improved usability and functionality while directly addressing the course outcome by leveraging industry-standard tools, innovative techniques, and skills to deliver a valuable solution. 

&nbsp;&nbsp;&nbsp;&nbsp;The enhancement addressed another outcome by designing and delivering professional-quality communications tailored to specific audiences. This was achieved by adding comprehensive in-line code comments to describe functions, fields, and key code segments as well as program headers. A README, adapted from a CS-340 Client/Server Development template, was created using a markup file, providing GitHub repository essentials like installation instructions, code examples, and application screenshots, also created was a Unified Modeling Language (UML) class diagram illustrating the organization and relationships of classes. Additionally, an instruction manual was developed for non-technical stakeholders, with user-friendly application guidance.

&nbsp;&nbsp;&nbsp;&nbsp;To achieve the goal of building collaborative environments that enable diverse audiences to support organizational decision-making in computer science, a project charter was successfully implemented to establish clear communication and behavioral guidelines. The charter designated specific development tools, including Git for version control and GitHub as a remote repository, ensuring streamlined collaboration on technical tasks. It also outlined the use of Microsoft Teams for real-time meetings and discussions, facilitating effective communication among team members. Furthermore, the charter set behavioral expectations, such as minimizing side conversations and valuing diverse perspectives, which fosters an inclusive and respectful atmosphere. By integrating these tools and guidelines, the project created a cohesive and productive environment that empowers diverse teams to contribute to informed decision-making. This charter along with other documentation is stored in the documentation folder on GitHub.

&nbsp;&nbsp;&nbsp;&nbsp;The enhancement process was more complex than initially anticipated. Rather than a simple translation of the program from C++ to C#, the application underwent a fundamental transformation. Unlike a console application that runs sequentially in a loop, the enhanced application creates hundreds of objects and employs callbacks, data binding, and other mechanisms to connect use cases while maintaining a responsive user interface. 

&nbsp;&nbsp;&nbsp;&nbsp;Unforeseen challenges arose during development, including encryption issues, input validation, and missing properties. For instance, a new property, IsAdmin, had to be added to the user model to restrict account addition and removal to a single administrative account. Input validation to enforce unique usernames was overlooked initially and had to be added later. The most challenging aspect was serializing two data structures, a list of accounts, and a list of users, into a single string for storage. Key lessons learned included working with declarative markup languages for the views, implementing data binding and events in the view models, and mastering encryption and serialization in the models.

See the original artifact here [CS410 Artifact](https://github.com/mufg80/CS_410_ReverseEngineering)

See the enhancement here [CS410 Enhancement](https://github.com/mufg80/CS410_Enhancement_InvestmentAccounts)

## **Code Review**

{{< youtube pZR-EUxrckI >}}