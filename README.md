# Aircall

[![License](http://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/HazAT/badge/blob/master/LICENSE)
[![Gem](https://badge.fury.io/rb/aircall.svg)](https://rubygems.org/gems/aircall)

A Ruby gem for [Aircall](https://developer.aircall.io/api-references/).
Only some methods are presents for the moment.


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'aircall'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install aircall


## Usage

### Init

Create new Aircall connection like this:

    require 'aircall'
    aircall = Aircall.new({id: [AIRCALL_ID], token: [AIRCALL_TOKEN]})

Or like this:
    
    require 'aircall'
    aircall = Aircall.new
    aircall.id = [AIRCALL_ID]
    aircall.token = [AIRCALL_TOKEN]


### Methods

#### [Calls](./doc/calls.md)
#### [Numbers](./doc/numbers.md)
#### [Contacts](./doc/contacts.md)
#### [Users](./doc/users.md)

### Examples
`aircall.contacts.get_by_email("youremail@gmail.com")`

`aircall.contacts.get_by_phone_number("+33612345678", per_page:1, page:3, order: "desc", order_by: "updated_at")`

---

## Development

### Build
`gem build aircall.gemspec`

### Local installation
`gem install ./aircall[version].gem`


### Tests

Create **.env** file from **.env.example**.
Complete with your variables.
 
Run test with `rake test`. 


### Deployment

 Deployment from Github
 
`bundle exec rake release`