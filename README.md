# Spectral Sequence File Formats



We need several file formats: 
1. A Spectral sequence chart file format for the display 
2. A Spectral sequences data format for binary linear algebra data.
3. A Steenrod module file format (maybe also handle modules over other algebras?)
4. A chain complex format for derived modules (maybe joint with the Steenrod module file format?).
5. A run config format for the resolver?

I think we should try to distinguish between (1) Mathematical data defining a module and (2) configuration data saying what the resolver should do with the data.

The chart format should be suitable for handling in python, javascript (for browser),
and lua (for lualatex).
It would be good if it is possible to manipulate the module format without Rust bindings, but that is negotiable.
I expect all access to the back end format go through a foreign function interface to Rust.


We need to consider the tradeoffs between making breaking changes and preserving
mistakes. In interest of obtaining forwards compatibility it would be a good idea to come
up with an extensive list of reserved keywords and to require editors / viewers to crash as often as possible.
