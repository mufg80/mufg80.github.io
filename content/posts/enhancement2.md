+++
date = '2025-06-06T03:42:57-05:00'
draft = false
title = 'Data Structures and Algorithms Enhancement'
weight = 3
featured_image = "/images/enhancement2.png"
cover_dimming_class = "bg-white-10"
omit_header_text = true
+++
### Binary Search Tree Implementation

<!--more-->

{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;The artifact selected for enhancement was a console application written in C++ for CS-300 Data Structures and Algorithms, completed in 2024. It represents an important milestone in applying fundamental data structures and algorithms to real-world problems. Originally built with a vector-based approach, the program excelled in sorting and searching static data but was inefficient for dynamic environments. This limitation made it an ideal candidate for enhancement, offering an opportunity to study algorithmic efficiency while managing the trade-offs of different data structures. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;The application originally featured a menu that loaded a text file into memory as a list of college courses. Users could display a single course, view courses in sorted order, or exit the program. A C++ vector was used to store the list, leveraging quicksort and binary search algorithms to efficiently sort and retrieve data. However, the vector structure was suboptimal for frequent insertions, as adding elements, especially near the beginning, required the shifting of subsequent elements and resulted in O(n) time complexity in the worst case. By contrast, appending items to the end of the vector is O(1) but does not maintain the list’s sorted order. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;The program’s efficiency in a static environment was strong, with quicksort averaging O(n log n) complexity and binary search running at O(log n) complexity. However, frequent insertions caused the need for re-sorting, which diminished the structure’s viability in dynamic scenarios. To optimize insertion efficiency, a binary search tree (BST) was implemented, offering O(log n) insertion and search time complexity while maintaining sorted order. Unlike the vector, an in-order traversal of the BST automatically produces a sorted list without requiring repeated sorting operations. To further enhance performance, automatic rebalancing was introduced to prevent degradation in unbalanced trees. Although rebalancing has O(n) complexity, it occurs significantly less frequently than the vector’s mandatory quicksort re-sorting, making it a worthwhile trade-off for managing dynamic data. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;This enhancement shows proficiency in algorithms and data structures because it required the development of a custom BST and associated algorithms. To achieve this, a node class was created to store course information as well as a binary tree class to manage parent/child relationships. Additionally, algorithms for depth-first traversal, tree rebalancing, and insertion were developed to optimize data handling. Furthermore, data validation was rewritten for the BST, ensuring that each course object included an ID, description, and a list of prerequisites, all of which were verified against existing courses in memory. Finally, the enhancement refined algorithmic recursion skills, as many tree operations such as depth-first search, node insertion, height calculation, and tree clearing relied on recursive functions. Implementing these algorithms deepened the understanding of recursion, function calls, and pointer management. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;Beyond technical improvements, the enhancement addressed outcome two: “Design, develop, and deliver professional-quality oral, written, and visual communications that are coherent, technically sound, and appropriately adapted to specific audiences and contexts.” This outcome was met through several actions:

{{</paragraph>}}
{{<bullet>}}

Comprehensive in-line code comments were added, describing functions, fields, and key code segments. Care was taken to avoid stating the obvious and instead highlighted overarching goals, such as input validation logic.

{{</bullet>}}
{{<bullet>}}

Headers were added to all four source code files to clarify the intention of each file.

{{</bullet>}}
{{<bullet>}}

A README was created using a markup file, adapted from the template learned in CS 340 Client/Server Development. This README addresses common informational needs in a GitHub repository, such as installation and “getting started” instructions, and includes C++ code examples and application screenshots for clarity. 

{{</bullet>}}
{{<bullet>}}

A Unified Modeling Language (UML) class diagram was developed, illustrating the binary search tree and node classes as well as the course structure.

{{</bullet>}}
{{<bullet>}}

An instruction manual was created for non-technical stakeholders, such as students and advisors at ABC University, providing easy-to-understand instructions to assist with application use. These documents are stored in the repository’s documentation folder.

{{</bullet>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;This enhancement successfully met the course outcome outlined in Module One: “Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution, while managing the trade-offs involved in design choices.” 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;The analysis of trade-offs and performance was demonstrated through a vector versus BST comparison, weighing insertion efficiency against rebalancing costs. The implementation of recursion was critical for the tree’s traversal, insertions, and height calculations, improving algorithm efficiency while reinforcing recursive problem-solving skills. Memory management was enhanced by introducing unique pointers to ensure safe memory allocation and ownership handling, eliminating potential leaks and improving stability.

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;The manual development of the BST from scratch required designing node relationships, recursive functions, and validation logic, going far beyond the basic use of C++ vectors. Moreover, the BST class is properly encapsulated, exposing only a few public functions while keeping most of its inner workings private to protect its state. As a result, the program became responsive to dynamic data needs, supporting real-time course additions while maintaining sorted order without expensive re-sorting, thus improving usability and adaptability for evolving datasets. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;More complex than anticipated, the enhancement process presented several challenges. One significant challenge was ensuring memory safety by using modern C++ practices, such as, replacing raw pointers with unique pointers. While they improved safety, their ownership model introduced a learning curve, requiring additional node class functions to manage ownership transfers properly. Recursive functions also required strategic adjustments, such as using references instead of return values, which simplified algorithm logic and improved efficiency by minimizing unnecessary argument passing. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;Additionally, analyzing trade-offs between vectors and BSTs deepened the understanding of Big O notation, highlighting the benefits and limitations of each structure in dynamic environments. By designing a dedicated BST header and implementation file, the project became more readable, modular, and significantly easier to debug. 

{{</paragraph>}}
{{<paragraph>}}

&nbsp;&nbsp;&nbsp;&nbsp;Beyond meeting course objectives, this project reinforced industry-relevant skills in designing scalable solutions and their accompanying documentation. The challenges, particularly in mastering recursion and memory management, led to a greater understanding of programming techniques, enhancing both theoretical knowledge and practical implementation. Ultimately, this enhancement serves as a testament to growth in algorithmic problem-solving, computational efficiency, and professional coding practices, valuable assets for future technical endeavors.

{{</paragraph>}}

See the original artifact here [ABCUapp](https://github.com/mufg80/CS300_ABCU_App)

See the enhancement here [ABCUApp Enhanced](https://github.com/mufg80/CS300_Enhancement2)

## **Code Review**

{{<youtube u8fgrFfOLN8>}}