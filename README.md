# clsQueueArray <a href=""><img align="right" src="https://img.shields.io/badge/C++-17-blue.svg?style=flat-square" alt="C++17"></a>

**A modern, efficient, and easy-to-understand generic Queue implementation in C++ using `clsDynamicArray` as the underlying container.**

Ideal for:
- Students learning Data Structures & Algorithms
- Developers needing a lightweight, header-only queue with extra utilities
- Projects that value clean, readable, and well-documented code

## Features

| Feature                    | Complexity | Description                                      |
|----------------------------|------------|--------------------------------------------------|
| `push` / `insert_back`     | **O(1)**   | Add element to the back                          |
| `pop`                      | **O(1)**   | Remove element from the front (amortized)        |
| `front()` / `back()`       | O(1)       | Access first or last element                     |
| Random access `get(i)`     | O(1)       | Direct index access (thanks to array backend)    |
| `insert_after(index, val)` | O(1)       | Insert after any position                        |
| `insert_front`             | O(n)       | Push to front (useful for deque-like behavior)   |
| `reverse()`                | O(n)       | Reverse the entire queue in-place                |
| `update(index, val)`       | O(1)       | Modify any element by index                      |
| `size()`, `empty()`        | O(1)       | Fast status checks                               |
| Fully generic              | ✔          | Works with any type (`int`, `string`, custom classes, etc.) |

## Why clsQueueArray?

- **Header-only** – just `#include "clsQueueArray.h"` and you're ready.
- Built on top of the battle-tested `clsDynamicArray` (automatic resizing, no manual memory management).
- Extremely readable code – perfect for educational purposes while still being performant.
- Extra utilities not present in standard `std::queue` (random access, reverse, insert-after, etc.).
- Zero external dependencies.

## Quick Example

```cpp
#include "clsQueueArray.h"
#include <iostream>

int main() {
    clsQueueArray<int> q;

    q.push(10);
    q.push(20);
    q.push(30);

    q.print();          // 10 20 30
    std::cout << "Front: " << q.front() << "\n";  // 10
    std::cout << "Back:  " << q.back()  << "\n";  // 30

    q.insert_after(1, 99);
    q.print();          // 10 20 99 30

    q.reverse();
    q.print();          // 30 99 20 10

    q.pop();
    q.print();          // 99 20 10

    return 0;
}
Installation
Just copy the two files into your project:
textclsDynamicArray.h
clsQueueArray.h
Include and use instantly – no build system changes required.
Requirements

C++17 or later (for class template argument deduction and std::cout improvements)

License
MIT © 2025 – Feel free to use, modify, and distribute.

⭐ If you find this library helpful, give it a star! It helps others discover clean educational code.
textThis README is professional, highlights the real advantages (speed, extra features, educational value), and stays visually appealing on GitHub. Ready to copy-paste!
