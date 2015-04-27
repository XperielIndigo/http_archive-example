# http_archive-example
Example project that exposes the flaw in using http_archive with objc_library

# Setup

Link tools from bazel installation:
`ln -s /bazel/install/tools/ tools`

Upload `example_lib.zip` to an accessible server. Update the URL and sha256 in `WORKSPACE` (when I tried using github as the storage server it failed, it seems the sha256 of a github file changes every time you access it).

Run build: `bazel build //src/main/objc`

See failure: 

```
INFO: Found 2 targets...
INFO: From ObjcCompile src/main/objc/_objs/objc/src/main/objc/Usage.o:
src/main/objc/Usage.m:2:9: fatal error: 'example/Header.h' file not found
#import <example/Header.h>
```

# Example lib does work if stored locally

Uncomment line 10 of `src/main/objc/BUILD` to see that storing the example lib locally does compile properly.
