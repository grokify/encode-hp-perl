Encode::HP Perl
===============

[![CPAN version][version-svg]][version-link]
[![Build Status][build-status-svg]][build-status-link]
[![Docs][docs-metacpan-svg]][docs-metacpan-link]
[![License][license-svg]][license-link]

## NAME

`Encode::HP` - Extra sets of HP encodings

## VERSION

This document describes version 0.03 of Encode::HP, released September 15, 2013.

## SYNOPSIS

```perl
use Encode;
use Encode::HP;
 
# Greek8
$greek8 = encode("hp-greek8", $utf8);
$utf8 = decode("hp-greek8", $greek8);
```

## DESCRIPTION

Perl 5.7.3 and later ship with with hp-roman8 encoding, however, there are additional HP encodings that are unsupported but may be encountered; hence, this CPAN module tries to provide the rest of them.

## ENCODINGS

This version includes the following encoding tables:

Canonical   | Alias
------------|----------------
hp-greek8   | /\bgreek8$/i
hp-roman9   | /\br(oman)?9$/i
hp-thai8    | /\bthai8$/i
hp-turkish8 | /\bturkish8$/i

This version also adds the following alises:

Canonical | Alias
----------|----------------
hp-roman8 | /\br(oman)?8$/i

## UNSUPPORTED ENCODINGS

The following are unsupported due to the lack of mapping data.

```
'8'  - arabic8, hebrew8, and kana8 
'15' - japanese15, korean15, and roi15
```

If you have this information or access to an HP-UX system, please consider providing this data. Information on how to generate this data from an HP-UX system is available here:

http://sourceware.org/bugzilla/show_bug.cgi?id=5464.

## SEE ALSO

1. `glibc` charmaps: https://sourceware.org/git/?p=glibc.git;a=tree;f=localedata/charmaps
1. Generating a charmap from HP-UX: http://sourceware.org/bugzilla/show_bug.cgi?id=5464

Encode

## ACKNOWLEDGEMENTS

Maps for `hp-greek8`, `hp-roman9`, `hp-thai8`, and `hp-turkish8` are generated from `glibc` charmaps.

## CONTRIBUTIONS

Any reports of problems, comments or suggestions are most welcome.

Please report these on [Github](https://github.com/grokify/encode-hp-perl)

## AUTHORS

John Wang <johncwang@gmail.com>

## COPYRIGHT

Copyright 2013-2016 by John Wang <johncwang@gmail.com>.

This software is released under the MIT license cited below.

## LICENSE

Encode::HP is available under an MIT-style license. See [LICENSE](LICENSE) for details.

Encode::HP &copy; 2013-2016 by John Wang

 [version-svg]: https://badge.fury.io/pl/Encode-HP.svg
 [version-link]: https://badge.fury.io/pl/Encode-HP
 [build-status-svg]: https://travis-ci.org/grokify/encode-hp-perl.svg?branch=master
 [build-status-link]: https://travis-ci.org/grokify/encode-hp-perl
 [docs-metacpan-svg]: https://img.shields.io/badge/docs-metacpan-blue.svg
 [docs-metacpan-link]: https://metacpan.org/pod/Encode::HP
 [license-svg]: https://img.shields.io/badge/license-MIT-blue.svg
 [license-link]: https://raw.githubusercontent.com/grokify/encode-hp-perl/master/LICENSE