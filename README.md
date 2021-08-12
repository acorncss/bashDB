Name: BashDB

Use: bashDB is a library of functions that make it easy to store BASH variables  and arrays for future use.

Donation: If you use bashDB a donation would be appreciated. Give according to your means.
https://www.paypal.com/donate?hosted_button_id=P8USAAG7U2T28

Usage:
* Variables can be stored as strings, integers, indexed arrays, associative arrays. They can be stored as read-only but that is not recommended.
* Variables are stored in files (tables). The tables can be simple name-value tables or complex tables by using associative arrays.
* Files are stored in directories (DB's).
* Recommended variable naming is "dir_file_variableName". This makes it really easy to see where a variable comes from (and if changed) where to save it too.
* Firstly edit bdbLocation to be the root directory where all DB's are stored, this is a complete path so start and end with forward slash.
* Your script and bashDB can be located anywhere. Use "source bashDB" to use this library in your script.
* BDBcreate <dir/file> creates your first DB. It will create the directories if necessary.
* BDBinsert <dir/file> <var name> <var value> <attributes> will insert your first record.
* BDBdelete <dir/file> <var name> will delete a record.
* BDBupdate <dir/file> <var name> <new var value> <new attributes> will delete then insert a record with the same name and a new value.
* BDBselectAll <dir/file> will insert all variables from a file into your script.
* BDBselectRow <dir/file> <var name> will insert one variables into your script.
* BDBunset <dir/file> will unset all variables in your script from the named file.
* BDBclean <dir/file> just removes blank lines in files, if any appear.
* BDBdrop <dir/file> will delete the file but not the directory. File doesn't have to be empty.
* BDBgetVarArray <dir/file> just gets all variables from a file into an array. Useful if you have a complex DB and wish to iterate over those associative arrays.

Attributes:
'a' - indexed array
'A' - associative array
'i' - integer
r - read-only array or variable (ar Ar ir or just r for read-only string)
Just '' for a plain string variable (name="value"). An attribute is mandatory when indicated above.
All variables are declared as global.


