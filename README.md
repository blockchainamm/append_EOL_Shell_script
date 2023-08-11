# Shell script to append characters to End Of Line

This shell script permits the user to append characters at End Of Line (EOL) of a given file based on condition

The script first check if the file is present in the current working directory, if this file is present 
  - The character(s) given in the value variable is appended to the end of line
  - The append operation is done only for the lines satisfying the condition
    For example in the given script if the line ends with a number (condition g/[0-9]/) value a character of \ is appended to the End Of Line
    Note that for appending a single \, two \\ values should be assigned to the value variable

    ex  +"g/[0-9]/s/$/$value/g" -cwq $FileName

If the file is not present a prompt message is displayed stating that the file is not present in the current directory
