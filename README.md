# libutils example

## Instructions

### Download

```
$ git clone https://github.com/olehermanse/libutils_example.git
$ cd libutils_example
$ git submodule init
$ git submodule update
```

### Build dependency

```
$ cd libutils
$ git fetch --all --tags
$ ./autogen.sh
$ make -j32
```

### Build examples

```
$ ./autogen.sh
$ make -j32
```

## File size

Currently, the project has 2 versions of the same example - a program which prints `argv`.
One uses the `Seq` data structure from libutils (and allocation functions), the other does not use libutils at all.
After building with the steps above, you can compare the file size:

```
$ ls -al argv_printer*
-rwxr-xr-x  1 olehermanse  staff  10908 Jul 29 14:22 argv_printer_libs
-rwxr-xr-x  1 olehermanse  staff   9024 Jul 29 14:22 argv_printer_zero
```

(In this simple test, the library added 2K to file size).
