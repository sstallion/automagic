# GNU Auto~~tools~~magic

This repository contains reusable macros and auxiliary files for
[GNU Autotools][1]. It is intended as a simpler alternative to the
[GNU Autoconf Archive][2] and the [GNU Portability Library][3].

## Usage

Similar to the aforementioned projects, copy the files you wish to use
(preserving directory structure) and add the following macro calls to
`configure.ac`:

    AC_CONFIG_AUX_DIR([build-aux])
    AC_CONFIG_MACRO_DIRS([m4])

The following environment variable should also be added to the top-level
`Makefile.am` to add support for `aclocal` macros in Automake:

    ACLOCAL_AMFLAGS = -I m4

Some macros may have additional requirements; see comments in the macro
definition for more details.

## Contributing

Pull requests are welcome! If a problem is encountered using this repository,
please file an issue on [GitHub][4].

## License

Files in this repository are distributed under the terms of the Free Software
Foundation All-Permissive ([FSFAP][5]) license:

    Copying and distribution of this file, with or without modification,
    are permitted in any medium without royalty provided the copyright
    notice and this notice are preserved.  This file is offered as-is,
    without any warranty.

See [License Notices for Other Files][6] for more details.

[1]: https://www.gnu.org/software/automake/manual/html_node/Autotools-Introduction.html
[2]: https://www.gnu.org/software/autoconf-archive/
[3]: https://www.gnu.org/software/gnulib/
[4]: https://github.com/sstallion/automagic/issues
[5]: https://spdx.org/licenses/FSFAP.html
[6]: https://www.gnu.org/prep/maintain/html_node/License-Notices-for-Other-Files.html
