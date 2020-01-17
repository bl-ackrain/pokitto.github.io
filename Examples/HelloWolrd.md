---
title: Hello World
parent: Examples
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