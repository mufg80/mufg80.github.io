+++
date = '2025-06-06T03:43:00-05:00'
draft = false
title = 'Database Enhancement'
weight = 4
featured_image = "/images/enhancement3.png"
cover_dimming_class = "bg-white-10"
omit_header_text = true
+++
### Android Mobile Device RESTFul Service Implementation

<!--more-->

&nbsp;&nbsp;&nbsp;&nbsp;The artifact selected for this enhancement is an Android Studio application designed to manage inventory on a mobile device. The program features a login screen that allows users to register as new users and/or log in. After successful login, a main screen displays a list of inventory items, with each line showing the item’s name, description, and quantity. Additionally, each item includes three buttons for incrementing, decrementing, or deleting the item. The application uses SQLite, a serverless, lightweight, and self-contained Structured Query Language (SQL) database tailored for mobile device limitations. SQLite’s advantages ensure a seamless user experience while meeting mobile device constraints. 

&nbsp;&nbsp;&nbsp;&nbsp;Created in CS-360 Mobile Architecture & Programming at the end of 2024, this artifact was an ideal enhancement candidate, particularly through the integration of a remote database, which addressed the limitations of data storage on a mobile device. While SQLite is effective, it has inherent constraints that a remote server and Representational State Transfer (RESTful) service can overcome, adding significant value to the application in three significant ways:

- A remote server offers substantially more storage capacity than a mobile device, allowing users to preserve device memory for personal use. Applications that consume excessive memory face the risk of user deletion, so this enhancement increases the application’s appeal. 

- The Application Programming Interface (API) enables data access across multiple platforms, paving the way for future developments like a desktop application, which would allow synchronized inventory data across devices. 

- A server allows administrators to manage backups and data recovery, tasks often neglected by users, ensuring data preservation. 

- This enhancement modifies the database schema to allow users to query only their own items, making the application more versatile and user specific. Instead of sharing the same inventory of wall items for editing or deletion, a limitation of the original application, users can query the items specific to their respective work.

&nbsp;&nbsp;&nbsp;&nbsp;All planned enhancements were successfully implemented in this milestone. A remote Microsoft SQL Server was established, accessible through a RESTful service built using Microsoft’s Active Server Pages (ASP) framework, with database operations and Hypertext Transfer Protocol Secure (HTTPS) requests written in C#. The Android Studio project was updated as planned: The partially implemented text messaging functionality was removed, and items with zero quantity now trigger an on-screen notification. A toggle button was added to the menu, enabling users to switch between local and remote unsynchronized databases, allowing distinct items to be stored in each. The SQLite database was also modified to include a foreign key in the items table, linking each item to a specific user, enabling user-specific queries. Additionally, code was added to query the remote database via the RESTful service, refreshing the inventory view with the appropriate data when the database toggle is switched. 

&nbsp;&nbsp;&nbsp;&nbsp;The creation and modification of these databases demonstrated proficiency in several database-related skills, including schema design, query development, normalization, and optimization. Schema design involved creating tables and defining relationships, such as linking items to users via foreign keys to reduce redundant data storage. Queries for creating, reading, updating, and deleting (CRUD) data were designed to maintain data integrity while protections against SQL injections were added in both databases. Normalization techniques were applied to minimize redundancy and enhance data consistency, a critical skill as databases scale in complexity. Optimization techniques, such as appropriate data types, SQL features like auto-incrementing and non-null fields, and managing constraints, were employed to handle the datasets efficiently. 

&nbsp;&nbsp;&nbsp;&nbsp;Achieving the course’s five outcomes required more than just functional code with three outcomes specifically targeted in this enhancement. The first, to “employ strategies for building collaborative environments that enable diverse audiences to support organizational decision-making in the field of computer science,” was addressed through a project charter. Templated from CS-250 Software Development Lifecycle, the charter outlined the project’s vision, mission, behavioral rules, and communication guidelines, fostering a collaborative team culture. Tools like GitHub were used as a remote repository for code review, promoting early issue resolution. Tools like Microsoft Teams were recommended to facilitate live group chats for technical and non-technical members while GitHub Discussions provide a forum for project-related debates. A code review was conducted to help new team members understand the project’s scope and tasks, enhancing collaboration, by quickly bringing team members up to speed. 

&nbsp;&nbsp;&nbsp;&nbsp;The second outcome, to “design, develop, and deliver professional-quality oral, written, and visual communications that are coherent, technically sound, and appropriately adapted to specific audiences and contexts,” was achieved through multiple deliverables. A code review addressed the oral and visual requirements, covering the enhancements and project goals. A readme file, based on the CS-340 Client/Server Development template, included images and code examples to help developers quickly understand the project and receive instructions designed for environment installation and performance speed and ease. Substantive code comments, including headers, function descriptions, and inline notes, were added to both the Android and web API code for clarity. A user guide, created as a Hyper Text Markup Language (HTML) quick-reference document for non-technical users, addressed user input, errors, instructions, and limitations. Finally, two Unified Modeling Language (UML) class diagrams, created using plantUML.com, visually communicated the structure of the Android and web API applications. 

&nbsp;&nbsp;&nbsp;&nbsp;The fifth outcome, to “develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities, mitigate design flaws, and ensure privacy and enhanced security of data and resources,” was critical because of the public-facing web API. Security measures included username and password protection, a strong API key, SQL injection prevention, input validation, and encryption. Each user’s inventory items were linked to their unique login, preventing unauthorized access. The remote database was secured with an API key transmitted in the HTTPS header and validated by the RESTful service’s middleware, which rejects invalid requests before processing. Parameterized queries in both the mobile application and web API mitigated SQL injection risks by sanitizing inputs. Input validation in the mobile application’s user class and in the web API ensured data integrity by rejecting invalid entries. HTTPS encryption protects data in transit, and API keys are stored in configuration files, not source code, allowing periodic rotation in production environments. 

&nbsp;&nbsp;&nbsp;&nbsp;Creating this enhancement was challenging and time-consuming, both in coding and in creating documentation. Nevertheless, learning markdown and plantUML was worthwhile because it greatly improved documentation quality. Applying written skills in targeting both technical and non-technical audiences required brainstorming as both a developer and a user. Establishing HTTPS communication between applications required extensive research into Android emulators, ports, IP addresses, and certificate creation. 

&nbsp;&nbsp;&nbsp;&nbsp;For development, each application had to be configured to either use or require a self-signed certificate. For instance, when the mobile application runs on the emulator, localhost (127.0.0.1) is the emulator’s address; further research found documentation stating that 10.0.2.2 targets the host machine. Another interesting addition was learning to use dependency injection in the web API, which involves setting up the application to inject needed class members into the class through the constructor, allowing for a more loosely coupled application. 

&nbsp;&nbsp;&nbsp;&nbsp;Additionally and equally important were the SQL instructions needed to configure the server database. Unique instructions rarely used, such as table creation and adding SQL server authentication, required research. Configuration of the SQL authentication allowed the web API to use a connection string allowing for only read and write access to the database, following the principle of least privilege for greater security. These efforts and others deepened expertise in tools like Swagger, Microsoft SQL Server Management Studio, Visual Studio, and Android Studio, equipping me with valuable skills for future projects.
 
See the original artifact here [CS360 Mobile Architecture](https://github.com/mufg80/CS360_Mobile_Architecture_Programming)

See the enhancement here [CS360 Mobile Architecture Enhancement](https://github.com/mufg80/CS360_InventoryApp_Enhancement3)

See the RESTFul Service here [CS360 Remote Server Web API](https://github.com/mufg80/InventoryAppRemoteAPI)

## **Code Review**

{{< youtube XTElaa1ZQeg >}}
