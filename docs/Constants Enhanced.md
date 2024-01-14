
**Constants Enhanced** instructions are built-in NINA instructions that have been enhanced to allow the use of Expressions.  These instructions take the name of the existing NINA instruction and put a plus-sign (+) at the end.  More instructions will be enhanced in the future.

## Take Exposure +, Take Many Exposures +, and Smart Exposure +

These imaging instructions allow Expressions for number of exposures, exposure time, gain, offset, and dither.  In the examples below, the Constants used are defined elsewhere. *Note: Filter, and binning are planned for the future.*

![](Exposure.png)

## Trained Flat Exposure +, Trained Dark Flat Exposure +

These imaging instructions allow Expressions for number of exposures, gain, and offset.  In the examples below, the Constants used are defined elsewhere. *Note: Filter, and binning are planned for the future.*

![](Trained.png)

## Cool Camera +

This instruction can use Expressions both for the set temperature and duration.

![](Cool.png)

## Move Focuser Relative +

![](Focus.png)

## Switch Filter +

Allows use of a Constant or Variable to specify a filter.   Note that filter names are represented by variables named Filter_filterName, where *filterName* is the name of a filter without spaces or other punctuation.

## External Script +

This is fully documented elsewhere in this document.

## Wait for Time Span +

Allows use of Constant or Variable to specify a wait time (in seconds)

