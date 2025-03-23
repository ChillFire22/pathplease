# pathplease
A paths-only clipboard-like CLI tool to make remembering paths obsolete. Pipe the command and retrieve saved paths.

# Functionality
The command stores a file's path in an indexed file, then will output them based on the inputted index.
This tool will particularly shine with long paths names or the need to write multiple paths

# Examples
The following assumed the placeholder command name 'pp' (Path, please!) and subcommands are figurative
```
$ls
  foo.txt  bar.md  dir1 dir2
$pp foo.txt bar.md
$pp dir1
$pp --list
  Index) Path
  1)  /path/to/foo.txt
  2)  /path/to/bar.md
  3)  /path/to/dir1
$echo $"pp 1 3"
  /path/to/foo.txt  /path/to/dir1
$echo $"pp"
  /path/to/foo.txt  /path/to/bar.md  /path/to/dir1
$pp --clear
$echo $"pp"

$pp --list
  Index)  Path
  -
$pp /invalid/path/to/some/file
  Error: invalid path
```
# Extras
Any extra functionality is open to discussion and future implementation.
The first version, v-0.0.1, will serve as first prototype to demonstrate functionality and work as-is.

# Warning
This tool is provided as-is with no guarantees.
