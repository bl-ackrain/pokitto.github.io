---
title: Hello World
parent: C++
nav_order: 1
has_children: false
---


## Hello World

Your first program on the pokitto

```cpp
#include "Pokitto.h"
int main(){
    using PC=Pokitto::Core;
    using PD=Pokitto::Display;
    PC::begin();
    while( PC::isRunning() ){
        if( !PC::update() ) 
            continue;
        PD::print("hello world");
    }
    return 0;
}
```