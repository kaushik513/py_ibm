## Typecasting

float(2) will give 2.0
int(1.1) will give 1 
int('A') doesn't convert it to its ASCII for some reason
str(1) converts an int to a string. str(1):"1"

## Boolean

"Boolean" is a data type in Python. It can have two values - True or False (with the capital T and F). 
	type(True):bool
	int(True) is 1, bool(1) is True
	int(False) is 0, bool(0) is False

## Other notes

Print info about types with `sys.float_info`, `sys.int_info`, etc.

Strings can be represented as '' or "". Can't mix both though.

/ does float division.
// does integer division.