---
description: The documentation for Quick Redis
---

# Documentation

## Commands

* [add](docs.md#add)
* [delete](docs.md#delete)
* [get](docs.md#get)
* [has](docs.md#has)
* [set](docs.md#set)
* [subtract](docs.md#subtract)

{% hint style="info" %}
All commands work with dotted notation
{% endhint %}

## add\(_key_, _number_\) <a id="add"></a>

This command adds a number to a key in the Redis database \(if the key doesn't exist it will add from 0\)

```javascript
client.add('foo', 500).then(console.log) // -> 500
```

## delete\(_key_\) <a id="delete"></a>

This command deletes a key from the Redis database \(returns 0 if key doesn't exist, returns 1 if success\)

```javascript
client.set('foo', 'bar').then(console.log) // -> 'bar'

client.delete('foo').then(console.log) // -> 1
```

## get\(_key_\) <a id="get"></a>

This command returns the value of a key in the Redis database

```javascript
client.set('foo', 'bar').then(console.log) // -> 'bar'

client.get('foo').then(console.log) // -> bar
```

## has\(_key_\) <a id="has"></a>

This command checks if a key exists in the Redis database

```javascript
client.set('foo', 'bar').then(console.log) // -> 'bar'

client.has('foo').then(console.log) // -> true
```

## set\(_key_, _value_\) <a id="set"></a>

This command sets the value of a key in the Redis database

```javascript
client.set('foo', 'bar').then(console.log) // -> 'bar'
```

## subtract\(_key_, _number_\) <a id="subtract"></a>

This command subtracts a number from a key in the Redis database \(if the key doesn't exist it will subtract from 0\)

```javascript
client.subtract('foo', 500).then(console.log) // -> -500
```

