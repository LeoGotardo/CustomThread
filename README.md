---

# CustomThread

## Introduction

`CustomThread` is a custom threading class in Python that extends the functionality of the standard `threading.Thread` class. It allows for additional features such as returning the result of the target function and raising exceptions in the thread.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Installation

To use `CustomThread`, simply copy the class definition into your project. Ensure you have Python installed (version 3.x is recommended).

## Usage

```python
from custom_thread import CustomThread

def example_function(param1, param2):
    print(f"Parameters are {param1} and {param2}")
    return param1 + param2

# Create a CustomThread instance
thread = CustomThread(target=example_function, args=(5, 10))

# Start the thread
thread.start()

# Join the thread and get the return value
result = thread.join()
print(f"Result from thread: {result}")
```

## Features

- **Return Value**: The thread can return a value from the target function.
- **Exception Handling**: Allows raising exceptions in the thread.
- **Thread Identification**: Provides a method to get the thread ID.

## Dependencies

- Python 3.x
- ctypes module (included in the standard library)

## Configuration

No specific configuration is required. 

## Documentation

### Class: `CustomThread`

#### `__init__(self, group=None, target=None, name=None, args=(), kwargs={}, Verbose=None)`
Initializes a new `CustomThread` instance.

- **group**: Thread group.
- **target**: Target function to call when thread starts.
- **name**: Thread name.
- **args**: Arguments to pass to the target function.
- **kwargs**: Keyword arguments to pass to the target function.
- **Verbose**: Verbosity level (not used in the current implementation).

#### `run(self)`
Executes the target function with the given arguments and keyword arguments.

#### `join(self)`
Waits for the thread to finish and returns the result of the target function.

#### `get_id(self)`
Returns the ID of the respective thread.

#### `raise_exception(self)`
Raises an exception in the thread.

## Examples

See the [Usage](#usage) section for a basic example.

## Troubleshooting

- **Exception Raise Failure**: If raising an exception in the thread fails, an error message will be printed.
- **Return Value**: Ensure the target function returns a value if you intend to capture it using the `join` method.

## Contributors

- [LeoGotardo](https://github.com/LeoGotardo)

## License

This project is licensed under the MIT License.

---
