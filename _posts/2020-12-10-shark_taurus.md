---
layout: post
title: Installing SHARK on taurus
tags: [linux]
---

I have installed [shark](https://github.com/ICRAR/shark) on *taurus*, one of the big machines used by the Astronomy group at [CIAFF](http://www.ciaff.uam.es/ciaff/), [Universidad Autónoma de Madrid](http://www.uam.es). Here I explain the few issued found in the process.

Once I forked and cloned the repository locally, I followed the instructions from the documentation, getting the following error after trying `make all`

```
make[2]: *** No rule to make target '/usr/lib/libgsl.so', needed by 'libshark.so'.  Stop.
CMakeFiles/Makefile2:104: recipe for target 'CMakeFiles/sharklib.dir/all' failed
make[1]: *** [CMakeFiles/sharklib.dir/all] Error 2
Makefile:129: recipe for target 'all' failed
make: *** [all] Error 2
```

So, the problem seemed to be related with the gsl libraries. [Rodrigo Tobar](https://www.icrar.org/people/rtobar/) helped me investigating the issue. 

* We checked that the required gsl-dev libraries where installed:
```
dpkg-query -s libgsl-dev
```

* [shark](https://github.com/ICRAR/shark) compiles assuming that the gsl libraries are in `/usr/lib/libgsl.so`, and actually such a file exists in *taurus*, so we needed to check if that is the file to compile against. To do so, I listed the files that get installed by the package `libgsl-dev`:
```
dpkg-query -L libgsl-dev
```

* As I found out that the package actully installed the required gsl libraries in `/usr/lib/x86_64-linux-gnu/libgsl.so`, I compiled [shark](https://github.com/ICRAR/shark) with the following command:

```
cmake .. -DGSL_ROOT_DIR=/usr/lib/x86_64-linux-gnu/
```

This time I got the happy:
```
[100%] Built target shark
```