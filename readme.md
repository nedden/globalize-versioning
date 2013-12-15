# Globalize Versioning [![Build Status](https://travis-ci.org/globalize/globalize-versioning.png?branch=master)](https://travis-ci.org/globalize/globalize-versioning)

## Introduction

This gem provides an interface between versioning gems such as
[PaperTrail](https://github.com/airblade/paper_trail).

## Installation

````ruby
gem install globalize-versioning
````

## Usage

To add versioning
support to your model, just add the `:versioning => true` option to your
call to <code>translates</code>.  An example from our test suite:

```ruby
translates :title, :content, :published, :published_at, :versioning => true
```

You will also need to have already generated the versions table that `paper_trail`
expects.  See the paper_trail README for more details.

If you are adding globalize to any previously versioned models, please note
that you will need to add a new `locale` column to your versioning table.

Also, please see the tests in `test/globalize/versioning_test.rb` for some
current gotchas.

## License

See [LICENSE](LICENSE) for details.