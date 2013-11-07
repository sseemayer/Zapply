# zapply - Batch-run commands with zsh globbing and pattern matching

`za` is a tool for running a command on multiple files with the parameters specified to the program configurable by pattern matching. If you routinely work on many files whose filenames follow patterns, this might be a useful tool to you. No more long commandlines with combinations of `find`, `sed`, `awk`, `xargs`, etc.!

## Examples

	# Display all man pages starting with 'font' and their manpage sections
	$ za '/usr/share/man/man[0-9]/font(*).(*).gz' echo 'font$1 in section $2'

	# Move files into subdirectories according to their filename
	# ex. holiday_01.jpg holiday_02.jpg newyears_01.jpg newyears_02.jpg -> holiday/01.jpg holiday/02.jpg newyears/01.jpg newyears/02.jpg
	$ za '(*)_(*).jpg' mv '$f' '$1/$2.jpg'

## Installation

`za` requires only zsh. Just put it somewhere on your `$PATH`. There also is a manpage you might like to install.

## License
MIT
