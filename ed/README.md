## The JAARS "Ed" Editor
The `ed.chr` font in this directory comes from the DOS based "Ed" multilingua editor
that was also codeveloped, or at least heavily used by, the SIL.

The `ed.chr` font is in a binary format that may be non-standard when compared to
other `.chr` fonts.  Conversion to BDF is still possible using `bin2bdf` and 
`monobit-convert`.  The ed-bin2bdf.bdf font was produced by the `bin2bdf` utility
and is a partially successful conversion.

`monobit-convert` can be used to produce conversions with some success, using
command lines like:

`monobit-convert load -format=raw -cell=8x12 ed.chr -offset=10 -padding=12`

An approach to produce a complete BDF file is to generate bitmaps in BDF
format character-by-character where the `offset` parameter is changed incrementally
and `-count=1`, then unify the separate output files.
