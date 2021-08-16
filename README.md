## A sample gem example
> created using Ruby

For you to created a gems, use a file with gemspec extesion in your manager file and create a lib folder and a central file with rb extension. Look to the example down:

```bash
your_gem.gemspec

lib
    your_gem.rb
```

In your gemspec, follow the example down:

```bash
Gem::Specification.new do |s|
  s.name        = "your-gem_name"
  s.version     = "your-gem-version"
  s.summary     = "Your gem summary"
  s.description = "Your gem description"
  s.authors     = ["Your Name"]
  s.email       = 'your.email@your.domain'
  s.files       = ["lib/sample_gem.rb"]
  s.homepage    =
    'https://rubygems.org/gems/your-gem-locale'
  s.license       = 'MIT'
end
```

Created your own code in lib/sample_gem.rb. If you prefer follow the example:

```bash
class Example
  def self.word(word = "null word")
    puts word
  end
end
```

## Build your gem

Use a comand:

```bash
gem build sample_gem.gemspec
```

This command will generate a file with .gem extension. For use your created gem, use:

```bash
gem install your-file-version.gem
```

## Use your gem

After your gem install, type it **irb** in your Terminal and use:

```bash
require 'sample_gem'

Example.word
Example.word("test")
```
