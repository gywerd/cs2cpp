### cs2cpp
# From C# to C++

## Introduction

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

## Litterature
* Browning, J. B., & Sutherland, B. (2020). C++20 Recipes: A Problem-Solution Approach (2nd ed.). Apress, New York, NY.
* Gregoire, M. (2021). Professional C++ (5th ed.). Wiley, Hoboken, NJ.
* Kormanyos, C. (2021). Real Time C++: Efficient Object-Oriented and Template Microcontroller Programming (4th ed.). Springer-Verlag, Berlin.
* Lischner, R. (2020). Exploring C++20: The Programmer's Introduction to C++ (3rd ed.). Apress, New York, NY.
* Roth, S. (2021). Clean C++20: Sustainable Software Development Patterns and Best Practices (2nd ed.). Apress, New York, NY.
* Stroustrup, B. (2013). The C++ Programming (4th ed.). Pearson Education, Upper Saddle River, NJ.
* Stroustrup, B. (2018). A Tour of C++ (2nd ed.). Pearson Education, Upper Saddle River, NJ.

## Curriculum
##### _(minor edits might happen)_

- **Professional C++.** Ch. 1 (p. 3-86)
- **A Tour of C++.** Ch. 1 (p. 1-19)
- **The C++ Programming Language.** Ch. 1.2 (p. 37-58)
- **A Tour of C++.** Ch. 2 (p. 21-28)
- **Clean C++20.** Ch. 2-4 (p. 13-130)
- **C++20 Recipes.** Ch. 2 (p. 25-40)
- **Professional C++.** Ch. 2-3 (p. 87-167)
- **Exploring C++20.** Ch. 28 (p. 191-196)
- **Professional C++.** Ch. 4 (p. 87-167)
- **Exploring C++20.** Ch. 17-21 (p. 109-142)
- **C++20 Recipes.** Ch. 2 (p. 40-44)
- **Exploring C++20.** Ch. 30 (p. 203-209)
- **Professional C++.** Ch. 5-6; (p. 169-207)
- **Professional C++.** Ch. 8 (p. 250-282)
- **Exploring C++20.** Ch. 33-37 (p. 225-264)
- **Professional C++.** Ch. 9 (p. 283-335)
- **A Tour of C++.** Ch. 4 (p. 47-64)
- **Exploring C++20.** Ch. 39-40 (p. 275-294)
- **C++20 Recipes.** Ch. 2 (p. 55-80)
- **Exploring C++20.** Ch. 41 (p. 295-304)
- **A Tour of C++.** Ch. 3 (p. 29-46)
- **Exploring C++20.** Ch. 42-43 (p. 305-321)
- **Clean C++20.** Ch. 6 (p. 221-291)
- **A Tour of C++.** Ch. 5 (p. 65-77)
- **Professional C++.** Ch. 10 (p. 337-395)
- **Exploring C++20.** Ch. 38 (p. 265-273)
- **C++20 Recipes.** Ch. 6 (p. 189-213)
- **Professional C++.** Ch. 11 (p. 397-419)
- **The C++ Programming Language.** Ch. 1.3 (p. 59-85)
- **Professional C++.** Ch. 12 (p. 419-464)
- **A Tour of C++.** Ch. 6 (p. 78-92)
- **Exploring C++20.** Ch. 51-55 (p. 391-430)
- **C++20 Recipes.** Ch. 9 (p. 277-300)
- **A Tour of C++.** Ch. 7 (p. 93-105)
- **Exploring C++20.** Ch. 56 (p. 431-447)
- **Professional C++.** Ch. 13 (p. 465-494)
- **A Tour of C++.** Ch. 10 (p. 123-136)
- **Exploring C++20.** Ch. 14 (p. 95-98)
- **Exploring C++20.** Ch. 32 (p. 221-224)
- **Exploring C++20.** Ch. 60-61 (p. 491-509)
- **Professional C++.** Ch. 14 (p. 495-533)
- **Exploring C++20.** Ch. 48 Exceptions (p. 357-372)
- **Professional C++.** Ch. 15 (p. 536-572)
- **Exploring C++20.** Ch. 49-50 (p. 373-387)
- **Professional C++.** Ch. 16-18 (p. 535-698)
- **Exploring C++20.** Ch. 47 (p. 351-356)
- **A Tour of C++.** Ch. 8 (p. 107-110)
- **A Tour of C++.** Ch. 11 (p. 137-148)
- **C++20 Recipes.** Ch. 7 (p. 215-249)
- **A Tour of C++.** Ch. 12 (p. 149-162)
- **C++20 Recipes.** Ch. 8 (p. 251-276)
- **The C++ Programming Language.** Ch. 1.4 (p. 87-110)
- **Exploring C++20.** Ch. 45 (p. 327-340)
- **Professional C++.** Ch. 19 (p. 699-723)
- **Exploring C++20.** Ch. 44 (p. 323-326)
- **C++20 Recipes.** Ch. 2 (p. 44-55; 71-80)
- **Professional C++.** Ch. 20 (p. 725-761)
- **Clean C++20.** Ch. 5 (p. 131-219)
- **Clean C++20.** Ch. 7 (p. 293-334)
- **C++20 Recipes.** Ch. 11 (p. 365-428)
- **The C++ Programming Language.** Ch. 1.5 (p. 111-132)
- **C++20 Recipes.** Ch. 12-13 (p. 429-546)
- **Professional C++.** Ch. 21 (p. 763-791)
- **C++20 Recipes.** Ch. 2 (p. 55-60)
- **A Tour of C++.** Ch. 9 (p. 111-122)
- **Exploring C++20.** Ch. 63-64 (p. 525-548)
- **C++20 Recipes.** Ch. 2 (p. 60-71)
- **Exploring C++20.** Ch. 65-70 (p. 549-618)
- **Exploring C++20.** Ch. 73-74 (p. 643-655)
- **Professional C++.** Ch. 22-23 (p. 793-819)
- **Exploring C++20.** Ch. 46 (p. 341-350)
- **Professional C++.** Ch. 24-25 (p. 821-876)
- **Exploring C++20.** Ch. 8-11 (p. 49-76)
- **Exploring C++20.** Ch. 16 (p. 105-108)
- **Professional C++.** Ch. 26-28 (p. 877-971)
- **Professional C++.** Ch. 28 (p. 972-992)
- **Professional C++.** Ch. 7 (p. 211-247)
- **C++20 Recipes.** Ch. 10 (p. 301-363)
- **Exploring C++20.** Ch. 62 (p. 511-523)
- **Professional C++.** Ch. 29-30 (p. 993-1020)
- **Real-Time C++.** App. B.2 (p. 479-480)
- **Professional C++.** Ch. 30 (p.1021-1044)
- **Clean C++20.** Ch. 8 (p. 336-373)
- **Professional C++.** Ch. 31-34 (p. 1055-1161)
- **Real-Time C++.** Ch. 9 (p. 205-238)
- **Real-Time C++.** Ch. 11 (p. 279-294)
- **Real-Time C++.** Part III (p. 295-434)
- **Real-Time C++.** App. C (p. 493-492)
