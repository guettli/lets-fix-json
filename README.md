# Let's fix json

JSON is everywhere. A lot of specs got better during the last years (tcp, http, JavaScript), but up to now the fundamental important data interchange format JSON has not changed much.

## Long term goal: pluggable data types

If the sender and the receiver agree upon some data types, it should be simple to add new data types to JSON.

## Current step: Dream of fancy perferct future

How do we want it to be in the future?

Before consensus can be reached, the dream need to be written down.

## Later

??? up to now it is unclear how to update the specs. But I guess we will find a way.

## Feedback needed

Please tell me what you think:

- What do you want to add to JSON?
- Why do you prefer a different a different data format? Why do you think other formats are better?


Let's influence the future **together** :-)

Please create a new issue and tell us how you would like JSON to look like in the future: https://github.com/guettli/lets-fix-json/issues/new

### binary data type

There thousand ways to work around it. Very common is base64 encoding. But that's a useless work-around.

In Python you can create binary data with the "b" prefix. Example:

```
binary_data = b'\x00\xff....'
```

### add datetime

It would be nice to support it.

Other tools which support this:

* [PostgreSQL Date/Time](https://www.postgresql.org/docs/12/datatype-datetime.html#DATATYPE-DATETIME-INPUT)
* [Protobuf Timestamp](https://developers.google.com/protocol-buffers/docs/reference/google.protobuf#google.protobuf.Timestamp)
* [Python datetime](https://docs.python.org/3/library/datetime.html#datetime-objects)


### add timedelta

A timedelta datatype would be very nice.

Other tools which support this: 

* [PostgreSQL Interval](https://www.postgresql.org/docs/12/datatype-datetime.html#DATATYPE-INTERVAL-INPUT)
* [Protobuf Duration](https://developers.google.com/protocol-buffers/docs/reference/google.protobuf#duration)
* [Python timedelta](https://docs.python.org/3/library/datetime.html#timedelta-objects)

### add comments

Quoting @asb:

> Leave comments is essential for human beings understand what is going up.
> Is the best practice in any programming language.
> Is kind and nice for all who will study what is done.
> Every one knows that JSON was, -was- a encapsuled internal way to exchange data in javascript
> but now JSON is used do describe the data for all world.
> So, please make // into comments for JSON, let the spice flow.

Why HCL (HashiCorp Configuration Language) was invented:

> JSON ... is fairly verbose and most importantly doesn't support comments. 

Source: https://github.com/hashicorp/hcl

## Thanks

- People involved in the early discussion: https://es.discourse.group/t/json-add-datetime-timedelta-and-binary-data-types/134
