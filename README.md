# Simple C++ Timer Library
This library contains a simple timer implementation written in C++. 

## Tools 
* C++ 20
* CMake 

## Example Usage 
```
#include <functional>
#include <iostream>
#include <thread>
#include "../src/timer.hpp"

void main_loop() {
    std::this_thread::sleep_for(std::chrono::milliseconds(200));
}

int main() {

    timer timer;

    timer.setInterval<std::function<void()>>([]() {
        std::cout << "hello from another thread" << std::endl;
    }, 200);

    std::thread main_thread(main_loop);
    main_thread.join();
}
``` 

## LICENCE 
MIT