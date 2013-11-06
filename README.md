GDB pretty printers
===================

Conversion of the official pretty-printers for gdb for the version 3 of python.
Pretty printers allows to have nice print in gdb for STL containers.
To use it with gdb >= 7.6, you need to create in your home directory a file named .gdbinit containing the following lines :

    python
    import sys
    sys.path.insert(0, '/home/<personal folder>/git/gdb_pretty-printers/python')
    from libstdcxx.v6.printers import register_libstdcxx_printers
    register_libstdcxx_printers (None)
    end

Replace '/home/<personal folder>/git/gdb_pretty-printers/python' with the appropriate path of your git clone.
