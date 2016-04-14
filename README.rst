This is a Python package to hold the Windows executables used to make a Python
script runnable as a command on Windows.

To use one of these executables, make a copy of it called e.g. ``foo.exe``, and
place a Python script next to it called ``foo-script.py``. If the script
starts with a shebang (``#!C:\path\to\python.exe``), that will be launched. If
not, it assumes that ``python.exe`` is on ``%PATH%``.

The Python package exposes one function, ``find_exe``::

    from win_cli_launchers import find_exe
    # Get the path to one of the executables
    find_exe(arch='x86')
    find_exe(arch='x64')

These exes are part of `setuptools <https://github.com/pypa/setuptools>`__; this
package exists just to provide them without requiring the rest of setuptools.
They are released under the same MIT license as setuptools.
