# InvalidSelectedItemError

- extends: [InvalidOperationError](./doc/api/python/exceptions/invalidoperationerror.md)

**InvalidSelectedItemError is raised when a method call is valid for the object, but the set value is invalid for the object's current value. ex: can not select an invalid item for select item method.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [item](#item)

### message
- type: str

Message of the exception.


### stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### item
- type: str

Value set for the method.