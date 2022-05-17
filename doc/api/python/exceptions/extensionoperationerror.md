# ExtensionOperationError

- extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**ExtensionOperationError is raised when the specified extension with oparetion "install", "update", or "uninstall" failed.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [extention_type](#extention_type)
- [operation](#operation)

### message
- type: str

Message of the exception.


### stacktrace
- type: str

Stack of the exception which got raised inside the exception.


### extention_type
- type: str

Type of the extension.

### operation
- type: str

Operation of the extension.