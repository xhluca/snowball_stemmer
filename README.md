# `snowball-stemmer-wheels`

`snowball_stemmer_wheels` is a fork of `PyStemmer` that provides pre-built wheels for `PyStemmer` on `manylinux` for 3.6 to 3.12.

## What is PyStemmer?

> PyStemmer is a Python interface to the stemming algorithms from the Snowball
project (https://snowballstem.org/).
> 
> Snowball can generate pure-Python stemmer code, but if you want to stem a
lot of words this can be rather slow.
> 
> PyStemmer instead wraps the "libstemmer_c" library which is built from C
code generated by Snowball.
> 
> An alternative to using PyStemmer directly is to use the snowballstemmer
module from Snowball, which will automatically use PyStemmer if available,
falling back to the pure Python implementations if not.  This allows your
users to choose between the convenience of only dealing with pure Python
code and the significantly better performance of PyStemmer.

For more information, please check out the original repository: https://github.com/snowballstem/pystemmer

## Installation

To install `snowball-stemmer-wheels`, you can use `pip`:

```bash
pip install snowball-stemmer-wheels
```

To use inside python code:

```python
import snowball_stemmer

print("All available languages: ", snowball_stemmer.algorithms())

stemmer = snowball_stemmer.SnowballStemmer('english')
stemmer.stemWord('running')
# Output: 'run'
```

## License

PyStemmer is copyright (c) 2006, Richard Boulton, and is licensed under the MIT
license: see the file "LICENSE" for the full text of this.  It is was inspired
by an earlier implementation (which was copyright (c) 2001, Andreas Jung, and
also licensed under the MIT license, but no portions of which remain in this
package, and had a different API).

The snowball algorithms, and the snowball library, are copyright (c) 2001-2006,
Dr Martin Porter and Richard Boulton, and are licensed under the BSD license.
