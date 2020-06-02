### Guidelines for C++ Programming

- [**It is bad practice to use global variables in a shared library**](https://developercommunity.visualstudio.com/solutions/430480/view.html): A shared library can be unloaded while the application is running, and there may be no way to destroy a global variable. Thus when the application tries to access the global variable in the stack and can't find it, it looks in the heap. This causes an _access violation_
