This is a very simple package that uses Cython.
It shows how to "package" a Python package with compiled sources.

The source code is just the `.pyx` file (`integrate_f6.pyx`).

The other files are "metadata":

- [pyproject.toml](02-cython-distrib/pyproject.toml)
- [setup.py](02-cython-distrib/setup.py)

Exercise:

  0. have a look at the different files
  1. install the module
  3. make sure it can be imported from anywhere:
    
    cd /
    python -c 'import integrate_f6; print(integrate_f6)'
    
  4. call the `integrate_f6` function from the Python interpreter after importing the module

---

How to install:

The "old" way is to use setup.py:

    python setup.py build

or

    python setup.py build_ext --inplace

to compile the code.

---

The "new" way is to use `pip`:

    pip install --user .

To just build a distributable bundle:

    pip wheel .

This creates a binary "wheel" (zip archive) in `dist/` .

---
