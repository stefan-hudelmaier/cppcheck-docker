Docker image for cppcheck - a static analysis tool for C++

See <http://cppcheck.sourceforge.net>

This docker image might be useful for continuous integration scenarios
where one does not want to install cppcheck on all slave nodes.

# Available tags

* latest
* 1.71

# Usage

The directory with the source to be checked must be mounted as a volume under /src.
Parameters to cppcheck can be given after the name of the image.

```
sudo docker run -v $(pwd)/src:/src cppcheck --enable=all --xml --xml-version=2 2> /tmp/cppcheck.xml
```
