# encoding/json: implement type override for serialization

The fork adds the following APIs:
```
	func (*Encoder) Register(f interface{})
	func (*Decoder) Register(f interface{})
```
where f is a function that determines serialization for a specific type
and takes precedence over the MarshalJSON/UnmarshalJSON methods.

See: https://github.com/golang/go/issues/5901

It is forked from this MR:
https://go-review.googlesource.com/c/go/+/212998

