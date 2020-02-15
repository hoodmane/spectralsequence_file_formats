We need several file formats: 
A Spectral sequence chart file format for the display 
and a spectral sequences binary format for binary data from the back end.
A Steenrod module file format (maybe also handle modules over other algebras?)
The front end format should be suitable for handling in python, javascript (for browser),
and lua (for lualatex).
The back end format can be a bit more flexible because I expect all access to be through a
foreign function interface to Rust, so the only concern is that it should be as backwards
/ forwards compatible as possible.

We need to consider carefully the tradeoffs between making breaking changes and preserving
mistakes. In interest of obtaining forwards compatibility it would be a good idea to come
up with an extensive list of reserved keywords.
