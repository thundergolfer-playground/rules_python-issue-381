# rules_python-issue-381

Reproducing https://github.com/bazelbuild/rules_python/issues/381

### How to reproduce issue:

```bash
bazel run //reproduce_bug:main
```

**Output:** 

```bash
INFO: Analyzed target //reproduce_bug:main (0 packages loaded, 0 targets configured).
INFO: Found 1 target...
Target //reproduce_bug:main up-to-date:
  bazel-bin/reproduce_bug/main
INFO: Elapsed time: 0.094s, Critical Path: 0.00s
INFO: 1 process: 1 internal.
INFO: Build completed successfully, 1 total action
INFO: Build completed successfully, 1 total action
Traceback (most recent call last):
  File "/private/var/tmp/_bazel_jonathon/cb02cc81ca2b2c83ceff73c093dc1750/execroot/rules_python_demo/bazel-out/darwin-fastbuild/bin/reproduce_bug/main.runfiles/rules_python_demo/reproduce_bug/main.py", line 3, in <module>
    x = ciso8601.parse_datetime('2014-12-05T12:30:45.123456-05:30')
AttributeError: module 'ciso8601' has no attribute 'parse_datetime'
```



