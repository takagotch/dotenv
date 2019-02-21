### dotenv
---
.rb
https://github.com/bkeepers/dotenv

.js
https://github.com/motdotla/dotenv

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

```sh
npm install dotenv
yarn add dotenv

node -r dotenv/config your_script.js
node -r dotenv/config your_script.js dotenv_config_path=/custom/path/to/your/env/vars

DOTENV_CONFIG_<OPTION>=value node -r dotenv/config your_script.js
DOTENV_CONFIG_ENCODING=latin1 node -r dotenv/config your_script.js dotenv_config_path=/custom/path/to/.env
```

```js
require('dotenv').config()

DB_HOST=localhost
DB_USER=root
DB_PASS=s1mpl3

const db = require('db')
db.connect({
  host: process.env.DB_HOST,
  username: process.env.DB_USER,
  password: process.env.DB_PASS
})

const result = dotenv.config()

if (result.error) {
  throw result.error
}

console.log(result.parsed)

require('dotenv').config({ path: '/full/custom/path/to/your/env/vars' })

require('dotenv').config({ encoding: 'latin1' })

require('dotenv').config({ debug: process.env.DEBUG })

const dotenv = require('dotenv')
const buf = Buffer.from('BASIC=basic')
const config = dotenv.parse(buf)
console.log(typeof config, config)

const dotenv = require('dotenv')
const buf = Buffer.from('hello')
const opt = { debug: true }
const config = dotenv.parse(buf, opt)

const fs = require('fs')
const dotenv = require('dotenv')
const envConfig = dotenv.parse(fs.readFileSync('.env.override'))
for (let k in envConfig) {
  process.env[k] = envConfig[k]
}


const dotenv = require('dotenv')
const variableExpansion = require('dotenv-expand')
const myEnv = dotenv.config()
variableExpansion(myEnv)

import { Client } from 'best-error-reporting-service'
export const client = new Client(process.env.BEST_API_KEY)

import dotenv from 'dotenv'
import errorReporter from './errorReporter'

dotenv.config()
errorReporter.client.report(new Error('faq example'))
```

