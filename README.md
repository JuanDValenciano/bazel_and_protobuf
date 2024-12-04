# bazel_and_protobuf

Basic examples using protobuf with C++ example

## Getting setup

The scripts have everything you need to automate the construction process and run the container.

Build the Docker container:

```
$ ./scripts/build.sh
```

Run the container:

```
$ ./scripts/run.sh
```

Python files haven't dependencies. use a 3.4+ version.

## Compile examples with Bazel

To compile the two examples in the Cplusplus folder you must run:

```
$ bazel build //Cplusplus/add_people:hello_world
```

```
$ bazel build //Cplusplus/list_people:hello_world
```

## Using the example

In the workspace to add people to the address book use

```
$ ./bazel-bin/Cplusplus/add_people/hello_world db.bin
```

To view the data stored in db.bin 

```
$ ./bazel-bin/Cplusplus/list_people/hello_world db.bin
```