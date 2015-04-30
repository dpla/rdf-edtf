RDF::EDTF
=========

This is an `RDF::Literal` implementation around Extended Date Time Format.

The underlying EDTF parser and implementation is provided by
[`edtf-ruby`](https://github.com/inukshuk/edtf-ruby/).

Usage
-----

```ruby
require 'rdf/edtf'

RDF::EDTF::Literal.new('1076?')
# or
RDF::Literal('1076?', datatype: RDF::EDTF::Literal::DATATYPE)
```

Known Issues
------------

  - Datetimes without a zone offset will be parsed and reserialized as UTC with
    `+00:00`. See: https://github.com/inukshuk/edtf-ruby/issues/14
  - Sets will be reserialized with spaces in their separators. See:
    https://github.com/inukshuk/edtf-ruby/issues/15

Contribution Guidelines
-----------------------

Please observe the following guidelines:

  - Write tests for your contributions.
  - Document methods you add using YARD annotations.
  - Follow the included style guidelines (i.e. run `rubocop` before committing).
  - Use well formed commit messages.

Do note that in order for us to merge any non-trivial changes (as a rule of thumb, additions larger than about 15 lines of code), we need an explicit public domain dedication on record from you.

License
-------

This is free and unencumbered public domain software. For more information, see http://unlicense.org/ or the accompanying {file:UNLICENSE} file.