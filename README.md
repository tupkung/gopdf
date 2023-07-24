gopdf
=====

This repository was forked from https://github.com/signintech/gopdf to add some feature to fix the Thai font display issue. Which is about the render engine of embedding fonts in PDF. It can't use the complex script to display the correct glyph. So, in the short time to fix, I can do only to re-map the glyph index in some characters such as `maiEk-Thai`, `maiTho-Thai`, `maiTri-Thai`, `maiChattawa-thai`, `maiThanthakhat-thai` to the `*.small` glyph index.

By this solution, I must edit the code in `subset_font_obj.go` to use the new option type to change glyph index when AddChar() function is called.

