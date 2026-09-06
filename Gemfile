# frozen_string_literal: true

source "https://rubygems.org"

# Specify runtime dependencies in the gemspec
gemspec

# Specify development dependencies below
gem "rubocop-minitest", ">= 0.39.0", require: false
gem "rubocop-rake", require: false
gem "rubocop-shopify", ">= 2.18", require: false if RUBY_VERSION >= "3.1"

gem "puma", ">= 5.0.0"
gem "rack-cors"
gem "rackup", ">= 2.1.0"

gem "activesupport"
# Fix io-console install error when Ruby 3.0.
gem "debug" if RUBY_VERSION >= "3.1"
# Avoid i18n 1.15.0, which breaks on Ruby 3.1 (ruby-i18n/i18n#735).
gem "i18n", "!= 1.15.0"
# FIXME: Drop this once a json release includes https://github.com/ruby/json/pull/1072. json 3.0.0 and 3.0.1
# forward arguments after a leading parameter, syntax Ruby 2.7.3 was the first to parse, while allowing Ruby 2.7.0.
gem "json", "< 3" if RUBY_VERSION < "2.7.3"
gem "rake", "~> 13.0"
gem "sorbet-static-and-runtime" if RUBY_VERSION >= "3.0"
gem "yard", "~> 0.9"
gem "yard-sorbet", "~> 0.9" if RUBY_VERSION >= "3.1"

group :test do
  gem "event_stream_parser", ">= 1.0"
  gem "faraday", ">= 2.0"
  gem "jwt"
  gem "minitest", "~> 5.1", require: false
  gem "mocha"
  gem "webmock"
end
