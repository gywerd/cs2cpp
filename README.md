### cs2cpp
# From C# to C++

## Index
- [Introduction](#introduction)
	- [How can you contribute](#how-can-you-contribute)
	- [Major issues](#major-issues)
	- [Didactic considerations](#didactic-considerations)
- [Note Index](#note-index)
	- Part 1
	- Part 2
	- Part 3
	- Part 4
	- Part 5
	- Part 6
	- Part 7
	- Part 8
	- Part 9
- [Litterature](#litterature)
- [Study Plan](#study-plan)

## Introduction

This repo is intended as an aid for experienced C# programmers transitioning to C++. It is comprehensive, but not conclusive for everyone, as it follows my learning path and the curriculum I've developed for myself. There might be overlap between content of books resulting in minor adjustments of the curriculum over the course of time.

### How can you contribute
Suggestions can be reported as issues e.g. 
- other or better litterature
- clarificiation to notes

### Major issues
1. The transition from C# to C++ involves understanding the differences and similarities between the two languages, as well as adapting to C++'s manual memory management and more flexible nature.
2. Avoid Pointers in C++ where applicable. Pointers were a fundamental part of C++ and have a broader range of applications than just hardware control. They are used for dynamic memory management, data structures, function pointers, efficiency, and more.
3. Modern C++ practices emphasize safer and more abstract methods of memory management, including the use of automatic variables, smart pointers, the standard library, and references.
4. You can develop Business Applications in C++ without focusing heavily on pointers, especially by using modern techniques and leveraging abstract constructs and smart pointers.
5. **Learning process.** Mastering C++ requires patience, practice, and time. Use resources like online tutorials, books, and courses to build your understanding. Practical exercise and gradually increasing complexity are the keys to success.
6. **Projects and community.** Build small projects and participate in the programming community to share your progress and receive support from other developers.
7. **Useful namespaces.** Using `<string>`, `<vector>`, `<map>`, `<list>`, `<ctime>`, `<iostream>`, `<cstddef>`, and `using namespace std` provides access to functions and classes in the standard library – and it's easier to work with them similarly to using System, etc., in C#.
8. `<string>` is necessary for accessing the `std::string` type and string manipulation.
9. `<iostream>` is similar to System.IO and is necessary for accessing `std::cin` and `std::cout` for keyboard input and terminal output – will be included in std from C++23.
10. `<ctime>` provides access to functions like `std::time` and `std::localtime`, as well as struct `std::tm` and type `std::time_t` for working with dates and times.
11. `<fstream>` contains classes like `std::ifstream` and `std::ofstream`, which correspond to `File`, `StreamReader`, and `StreamWriter`, etc., in `System.IO`.
12. `<vector>`, `<map>`, `<list>`, etc., are used to work with vectors, maps, and lists in a similar way as `List<T>`, `Dictionary<TKey, TValue>`, etc., in `System.Collections.Generic`.
13. There isn't a direct equivalent of `System.Linq` in C++, but `<algorithm>` provides access to a range of algorithms for working with collections.
14. The `<cstddef>` header contains definitions of types and functions used for pointer arithmetic, including the specific `byte` type as a semantic alternative to `unsigned char`.
15. Using `this->` instead of `this` allows you to specifically refer to member variables in the class, which can help you avoid potential conflicts.
16. **Elimination of new.** Modern C++ practices encourage the use of smart pointers and automatic memory management to reduce the risk of memory leaks.
17. **Challenges with headers.** Use C++ modules instead of headers.
18. **Challenges with properties.** Learn how C++ handles properties compared to C#.
19. **No extension methods.** Use `string ToString(int i) { … }` instead of `string ToString(this int i) { … }`. They can still be placed in an ext file for access from multiple classes. Simply use `ext::ToString(i)` instead of `i.ToString`.
20. **Property idiom:** C++ doesn't have built-in properties like C#, but the property idiom is used to create similar functionality using getter and setter methods. In dynamic libraries (libs) C++/CLI `__declspec(property(get = getBar, put = setBar)) string Bar` can be used.
21. **Reference qualifiers** for types like `-'&'` and `-'&&'` are important in C++, especially in constructors/methods, and are reminiscent of the use of `ref` and `out` in C# - e.g., `Foo (const string& strName) {…}` and `Foo bar(const string& strname) {…}`.

### Didactic considerations
Experienced C# programmers shifting to C++ can efficiently harness their existing repository. The [`Litterature`](#litterature) list cover basic to very advanced topics of C++20. The `Study Plan`[`Study Plan`](#study-plan) provides an optimal order for reading the content of the books, thus facilitating a structured and efficient learning path. The [`Note Index`](#note-index)section is provided for overview, insights and inspiration.

## Note Index
_(each part included as PDF-file)_

- [Part 1](Notes/CS2CPP_notes_part_1.pdf)
	- Professional C++. Ch. 1. A Crash Course in C++ and the Standard Library 
	- As this is a crash course, theres a lot to comprehend. Fortunately it is followed up later in the book etc.
- [Part 2](Notes/CS2CPP_notes_part_3.pdf)
	- A Tour of C++. Ch. 1. The Basics
	- The C++ Programming Language. Ch. 1.2. The Basics
	- A Tour of C++. Ch. 1. User Defined Types
- [Part 3](Notes/CS2CPP_notes_part_2.pdf)
	- Clean C++20. Ch. 2. Build a Safety Net
	- Clean C++20. Ch. 3. Be Principled
- [Part 4](Notes/CS2CPP_notes_part_4.pdf)
	- Clean C++20. Ch. 4. Basics of Clean C++
- [Part 5](Notes/CS2CPP_notes_part_5.pdf)
	- C++20 Recipes. Ch. 2. Initialization and Auto
	- Professional C++. Ch. 2. Working with Strings and String Views
	- Professional C++. Ch. 3. Coding with Style
	- Exploring C++20. Ch. 28. Documentation
	- Professional C++. Ch. 4. Designing Professional C++ Programs
- [Part 6](Notes/CS2CPP_notes_part_6.pdf)
	- Exploring C++20. Ch. 12. Conditions and Logic
- [Part 7](Notes/CS2CPP_notes_part_7.pdf)
	- _Exploring C++20. Ch. 17. Characters_
	- _Exploring C++20. Ch. 19. Case-Folding_
	- _Exploring C++20. Ch. 20. Writing Functions_
	- _Exploring C++20. Ch. 21. Functional Arguments_
	- C++20 Recipes. Ch. 2. Compile Time Constants
	- _Exploring C++20. Ch. 30. Custom Types_
	- Professional C++. Ch. 5. Design and Objects
	- Professional C++. Ch. 6. Designing for reuse
- [Part 8](Notes/CS2CPP_notes_part_8.pdf)
	- Professional C++. Ch. 8. Gaining Proficiency with Classes a nd Objects
	- _Exploring C++20. Ch. 33. Assignment and Initialization_
	- _Exploring C++20. Ch. 34. Writing Classes_
	- _Exploring C++20. Ch. 35. More About Member functions_
	- Exploring C++20. Ch. 36. Access Levels
	- _Exploring C++20. Ch. 37. Understanding Object-Oriented Programming_
- Part 9
	- ...
	
## Litterature
* Browning, J. B., & Sutherland, B. (2020). C++20 Recipes: A Problem-Solution Approach (2nd ed.). Apress, New York, NY.
* Gregoire, M. (2021). Professional C++ (5th ed.). Wiley, Indiana, IN.
* Kormanyos, C. (2021). Real Time C++: Efficient Object-Oriented and Template Microcontroller Programming (4th ed.). Springer-Verlag, Berlin, DE.
* Lischner, R. (2020). Exploring C++20: The Programmer's Introduction to C++ (3rd ed.). Apress, New York, NY.
* Roth, S. (2021). Clean C++20: Sustainable Software Development Patterns and Best Practices (2nd ed.). Apress, New York, NY.
* Stroustrup, B. (2013). The C++ Programming (4th ed.). Pearson Education, Upper Saddle River, NJ.
* Stroustrup, B. (2018). A Tour of C++ (2nd ed.). Pearson Education, Upper Saddle River, NJ.

## Study Plan
_(minor edits might happen)_

_Optional_ reading marked with _italics_ is `nice for reference` and may be skimmed or outright skipped at your own discretion.

- **Professional C++.** Ch. 1 (Gregoire 2021 pp. 3-86)
- **A Tour of C++.** Ch. 1 (Stroustrup 2018 pp. 1-19)
- **The C++ Programming Language.** Ch. 1.2 (Stroustrup 2013 pp. 37-58)
- **A Tour of C++.** Ch. 2 (Stroustrup 2018 pp. 21-28)
- **Clean C++20.** Ch. 2-4 (Roth 2021 pp. 13-130)
- **C++20 Recipes.** Ch. 2 (Browning and Sutherland 2020 pp. 25-40)
- **Professional C++.** Ch. 2-3 (Gregoire 2021 pp. 87-167)
- **Exploring C++20.** Ch. 28 (Lischner 2021 pp. 191-196)
- **Professional C++.** Ch. 4 (Gregoire 2021 pp. 87-167)
- _**Exploring C++20.** Ch. 17-21 (Lischner 2021 pp. 109-142)_
- **C++20 Recipes.** Ch. 2 (Browning and Sutherland 2020 pp. 40-44)
- _**Exploring C++20.** Ch. 30 (Lischner 2021 pp. 203-209)_
- **Professional C++.** Ch. 5-6; (Gregoire 2021 pp. 169-207)
- **Professional C++.** Ch. 8 (Gregoire 2021 pp. 250-282)
- _**Exploring C++20.** Ch. 33-35 (Lischner 2021 pp. 225-247)_
- **Exploring C++20.** Ch. 36 (Lischner 2021 pp. 249-257)
- _**Exploring C++20.** Ch. 37 (Lischner 2021 pp. 259-264)_
- **Professional C++.** Ch. 9 (Gregoire 2021 pp. 283-335)
- _**A Tour of C++.** Ch. 4 Stroustrup 2018 (Stroustrup 2018 pp. 47-64)_
- **Exploring C++20.** Ch. 39-40 (Lischner 2021 pp. 275-294)
- **C++20 Recipes.** Ch. 2 (Browning and Sutherland 2020 pp. 55-60)
- **Exploring C++20.** Ch. 41 (Lischner 2021 pp. 295-304)
- **A Tour of C++.** Ch. 3 (Stroustrup 2018 pp. 29-46)
- **Exploring C++20.** Ch. 42 (Lischner 2021 pp. 305-314)
- _**Exploring C++20.** Ch. 43 (Lischner 2021 pp. 315-321)_
- **Clean C++20.** Ch. 6 (Roth 2021 pp. 221-291)
- **A Tour of C++.** Ch. 5 (Stroustrup 2018 pp. 65-77)
- **Professional C++.** Ch. 10 (Gregoire 2021 pp. 337-395)
- **Exploring C++20.** Ch. 38 (Lischner 2021 pp. 265-273)
- **C++20 Recipes.** Ch. 6 (Browning and Sutherland 2020 pp. 189-213)
- **Professional C++.** Ch. 11 (Gregoire 2021 pp. 397-419)
- **The C++ Programming Language.** Ch. 1.3 (Stroustrup 2013 pp. 59-85)
- **Professional C++.** Ch. 12 (Gregoire 2021 pp. 419-464)
- **A Tour of C++.** Ch. 6 (Stroustrup 2018 pp. 78-92)
- **Exploring C++20.** Ch. 51-55 (Lischner 2021 pp. 391-430)
- **C++20 Recipes.** Ch. 9 (Browning and Sutherland 2020 pp. 277-300)
- **A Tour of C++.** Ch. 7 (Stroustrup 2018 pp. 93-105)
- **Exploring C++20.** Ch. 56 (Lischner 2021 pp. 431-447)
- **Professional C++.** Ch. 13 (Gregoire 2021 pp. 465-494)
- **A Tour of C++.** Ch. 10 (Stroustrup 2018 pp. 123-136)
- **Exploring C++20.** Ch. 14 (Lischner 2021 pp. 95-98)
- **Exploring C++20.** Ch. 32 (Lischner 2021 pp. 221-224)
- **Exploring C++20.** Ch. 60-61 (Lischner 2021 pp. 491-509)
- **Professional C++.** Ch. 14 (Gregoire 2021 pp. 495-533)
- **Exploring C++20.** Ch. 48 (Lischner 2021 pp. 357-372)
- **Professional C++.** Ch. 15 (Gregoire 2021 pp. 536-572)
- **Exploring C++20.** Ch. 49-50 (Lischner 2021 pp. 373-387)
- **Professional C++.** Ch. 16-18 (Gregoire 2021 pp. 535-698)
- **Exploring C++20.** Ch. 47 (Lischner 2021 pp. 351-356)
- **A Tour of C++.** Ch. 8 (Stroustrup 2018 pp. 107-110)
- **A Tour of C++.** Ch. 11 (Stroustrup 2018 pp. 137-148)
- **C++20 Recipes.** Ch. 7 (Browning and Sutherland 2020 pp. 215-249)
- **A Tour of C++.** Ch. 12 (Stroustrup 2018 pp. 149-162)
- **C++20 Recipes.** Ch. 8 (Browning and Sutherland 2020 pp. 251-276)
- **The C++ Programming Language.** Ch. 1.4 (Stroustrup 2013 pp. 87-110)
- **Exploring C++20.** Ch. 45 (Lischner 2021 pp. 327-340)
- **Professional C++.** Ch. 19 (Gregoire 2021 pp. 699-723)
- **Exploring C++20.** Ch. 44 (Lischner 2021 pp. 323-326)
- **C++20 Recipes.** Ch. 2 (Browning and Sutherland 2020 pp. 44-55; 71-80)
- **Professional C++.** Ch. 20 (Gregoire 2021 pp. 725-761)
- **Clean C++20.** Ch. 5 (Roth 2021 pp. 131-219)
- **Clean C++20.** Ch. 7 (Roth 2021 pp. 293-334)
- **C++20 Recipes.** Ch. 11 (Browning and Sutherland 2020 pp. 365-428)
- **The C++ Programming Language.** Ch. 1.5 (Stroustrup 2013 pp. 111-132)
- **C++20 Recipes.** Ch. 12-13 (Browning and Sutherland 2020 pp. 429-546)
- **Professional C++.** Ch. 21 (Gregoire 2021 pp. 763-791)
- **C++20 Recipes.** Ch. 2 (Browning and Sutherland 2020 pp. 55-60)
- **A Tour of C++.** Ch. 9 (Stroustrup 2018 pp. 111-122)
- **Exploring C++20.** Ch. 63-64 (Lischner 2021 pp. 525-548)
- **C++20 Recipes.** Ch. 2 (Browning and Sutherland 2020 pp. 60-71)
- **Exploring C++20.** Ch. 65-70 (Lischner 2021 pp. 549-618)
- **Exploring C++20.** Ch. 73-74 (Lischner 2021 pp. 643-655)
- **Professional C++.** Ch. 22-23 (Gregoire 2021 pp. 793-819)
- **Exploring C++20.** Ch. 46 (Lischner 2021 pp. 341-350)
- **Professional C++.** Ch. 24-25 (Gregoire 2021 pp. 821-876)
- **Exploring C++20.** Ch. 8-11 (Lischner 2021 pp. 49-76)
- **Exploring C++20.** Ch. 16 (Lischner 2021 pp. 105-108)
- **Professional C++.** Ch. 26-28 (Gregoire 2021 pp. 877-992)
- **Professional C++.** Ch. 7 (Gregoire 2021 pp. 211-247)
- **C++20 Recipes.** Ch. 10 (Browning and Sutherland 2020 pp. 301-363)
- **Exploring C++20.** Ch. 62 (Lischner 2021 pp. 511-523)
- **Professional C++.** Ch. 29-30 (Gregoire 2021 pp. 993-1020)
- **Real-Time C++.** Appendix B.2 (Kormanyos 2021 pp. 479-480)
- **Professional C++.** Ch. 30 (Gregoire 2021 pp.1021-1044)
- **Clean C++20.** Ch. 8 (Roth 2021 pp. 336-373)
- **Professional C++.** Ch. 31-34 (Gregoire 2021 pp. 1055-1161)
- **Real-Time C++.** Ch. 9 (Kormanyos 2021 pp. 205-238)
- **Real-Time C++.** Ch. 11 (Kormanyos 2021 pp. 279-294)
- **Real-Time C++.** Part III (Kormanyos 2021 pp. 295-434)
- **Real-Time C++.** Appendix C (Kormanyos 2021 pp. 493-492)
