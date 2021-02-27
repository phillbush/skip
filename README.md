Skip text between two strings
=============================

skip removes all of its input that is enclosed by
its two arguments. Example:

	$ echo '/* comment */ int main(void) { puts("hello world!"); /* print */ return 0; }' | skip '/\*' '\*/'
	 int main(void) { puts("hello world!");  return 0; }

This is an awk version of [pranomostro/skip](https://github.com/pranomostro/skip).

This version of skip is capable of handling regular expressions.
So, if the from/to delimiters contain metacharacters, escape them!

Usage
-----

	cat file | skip from to

License
=======

[MIT/X11 license](./LICENSE).
