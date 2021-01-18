---
description: A guide to quickredis-db
---

# Getting Started

## Installing [Quick Redis](https://npmjs.com/package/quickredis-db)

To install [Quick Redis](https://npmjs.com/package/quickredis-db) run the following command in your project folder

```bash
npm install quickredis-db
```

## Example of [Quick Redis](https://npmjs.com/package/quickredis-db)​ <a id="example"></a>

```javascript
// Creating the redis client
const redis = require('quickredis-db');
const client = redis.createClient();

client.once('ready', () => console.log('Connected to database'));

// Setting a value
client.set('foo', 'bar').then(console.log); // 'bar'

// Reading a value
client.get('foo').then(console.log); // 'bar'
```

