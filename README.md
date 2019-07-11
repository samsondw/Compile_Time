# Compile_Time
Calculate time of compilation (UNIX_TIMESTAMP) based on __TIME__ and __DATE__ macros.

/*
 * compile_time.h
 *
 * Created: 29.03.2018
 *
 * Authors:
 *
 * Assembled from the code released on Stackoverflow by:
 *   Dennis (instructable.com/member/nqtronix)    |   https://stackoverflow.com/questions/23032002/c-c-how-to-get-integer-unix-timestamp-of-build-time-not-string
 * and
 *   Alexis Wilke                                 |   https://stackoverflow.com/questions/10538444/do-you-know-of-a-c-macro-to-compute-unix-time-and-date
 *
 * Assembled by Jean Rabault
 *
 * UNIX_TIMESTAMP gives the UNIX timestamp (unsigned long integer of seconds since 1st Jan 1970) of compilation
 * from macros using the compiler defined __TIME__ and __DATE__ macros.  This should include Gregorian calendar leap days,
 * in particular the 29ths of February, 100 and 400 years modulo leaps.
 *
 * The macro is based on __TIME__ and __DATE__, which are assumed to be formatted "HH:MM:SS" and "MMM DD YYYY", respectively.
 * The actual value can be calculated by the C compiler at compile time as all inputs are literals.
 * MAKE SURE TO ENABLE OPTIMISATION!
 *
 * Careful: __TIME__ is the local time of the computer, NOT the UTC time in general!
 */

To Use:
#include <compile_time.h>
time_t compile_time = UNIX_TIMESTAMP;
