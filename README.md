# ScrapBook

## Readings
[An Introduction to Modern CMake](https://cliutils.gitlab.io/modern-cmake/)
[Wait-free and lock-free programming](https://github.com/rigtorp/awesome-lockfree)
[`Book` C++ Concurrency in Action](https://www.bogotobogo.com/cplusplus/files/CplusplusConcurrencyInAction_PracticalMultithreading.pdf)
[`Thesis` Robustly Modelling World from Photos, Cornell University, 2016](https://pdfs.semanticscholar.org/5262/8c0c25f596f932b3ecf2061d905c1c690bb0.pdf)

## Resources
[Jemalloc memory allocator](http://jemalloc.net/)
[Git Magic - Stanford](http://www-cs-students.stanford.edu/~blynn/gitmagic/index.html)

## Hands-On

#### Valgrind ([man-page](https://linux.die.net/man/1/valgrind))
`sudo  apt-get install valgrind`

Memcheck
```bash
valgrind --leak-check=full \
         --show-leak-kinds=all \
         --num-callers=40 \
         --read-var-info=yes \
         --track-origins=yes \
         --trace-children=yes \
         --time-stamp=yes \
         --verbose \
         --demangle=yes \
         --log-file=valgrind-out.txt \
         --xml=yes \
         --xml-file=XMLFile.log \
         ./executabe args...
```
`valkyrie -l XMLFile.log`

Callgrind ([example](https://baptiste-wicht.com/posts/2011/09/profile-c-application-with-callgrind-kcachegrind.html))
`valgrind --tool=callgrind ./executable args...`
