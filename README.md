xprintfc
========

Most completed and little printf like subsystem for embedded system.

Example of code size now 2 architecture with all features enabled, compiled with -O3 :

    Embedded 32 bit ARM : 2268 bytes
    Linux X64 : 3690 bytes

 - Tested on microprocessor from 8 to 64 bit
 - Optional support for floating point number
 - Optional support for long long number
 - Support for binary number (%b)
 - Support for boolean value (%B)
 - Support for pointer in hex format (%p/%P)
 - Support for size_t C99 argument size
 - No library function required
 - Parametric function to emit single char
 - Configurable using config.h and -DHAVE_CONFIG_H
 - 10% fastest than libc functions.
 - And much more


Configurable options
========================================================================

The option can be set directly on the compiler command line
for example :
  gcc -DXCFG_FORMAT_LONGLONG=0 -c xformatc.c
compile the function without floating point support or inserted
in the file config.h and define the symbol HAVE_CONFIG_H on
compilation time.


XCFG_FORMAT_LONGLONG    Set to 0 to exclude support for long long.

XCFG_FORMAT_STATIC      Set to static to reduce stack usage only
                        for mono thread application.

XCFG_FORMAT_FLOAT       Set to 0 to exclude support for floating point.


XCFG_FORMAT_FLOAT_PREC	Set to 1 to make calculation using float instead of double.
