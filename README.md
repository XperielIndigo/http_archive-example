# http_archive-example
Example project that exposes the flaw in using http_archive with objc_library

# Setup

Link tools from bazel installation:
`ln -s /bazel/install/tools/ tools`

Run build: `bazel build //src/main/objc`

See failure: 

```
INFO: Found 2 targets...
INFO: From ObjcCompile src/main/objc/_objs/objc/src/main/objc/Usage.o:
src/main/objc/Usage.m:2:9: fatal error: 'example/Header.h' file not found
#import <example/Header.h>
```
