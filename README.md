### dotenv
---
.rb
https://github.com/bkeepers/dotenv

.java
https://github.com/shyiko/dotenv
```
gem 'dotenv-rails', groups: [:development, :test]
bundle

dotenv ./script.rb
dotenv -f ".env.local,.env" ./script.rb

```

```ruby
# config/application.rb
Bundler.require(*Rails.groups)
Dotenv::Railtie.load
HOSTNAME = ENV['HOSTNAME']

gem 'dotenv-rails', require: 'dotenv/rails-now'
gem 'gem-that-requires-env-variables'

gem install dotenv

require 'dotenv/load'

require 'dotenv'
Dotenv.load

require 'dotenv'
Dotenv.load('file1.env', 'file2.env')

require 'dotenv/tasks'
task mytask: :dotenv do 
end

S3_BUCKET=YOURS3BUCKET
SECRET_KEY=YOURSECRETKEYGOESHARE

config.fog_directory = ENV['S3_BUCKET']

export S3_BUCKET=YOURS3BUCKET
export SECRET_KEY=YOURSECRETKEYOGESHERE

PRIVATE_KEY="------BEGIN RSA PRIVATE KEY-------\nHkVN9...\n-----END DSA PRIVATE KEY----\n"
PRIVATE_KEY="------BEGIN RSA PRIVATE KEY-----
...
HkVN9...
...
--------END DSA PRIVATE KEY------"

DATABASE_URL="postgres://$(whoami)@localhost/my_database"

PASSWORD='pas$word'

SECRET_KEY=YOURSECRETKEYGOESHERE
SECRET_HASH="something-with-a-#-hash"

# config/initializers/dotenv.rb
Dotenv.require_keys("SERVICE_APP_ID", "SECRET_KEY", "SERVICE_SECRET")

```

```
```

