# Python MCStatus

[![PyPI - Version](https://img.shields.io/pypi/v/python-mcstatus.svg)](https://pypi.org/project/python-mcstatus)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/python-mcstatus.svg)](https://pypi.org/project/python-mcstatus)
[![Hatch project](https://img.shields.io/badge/%F0%9F%A5%9A-Hatch-4051b5.svg)](https://github.com/pypa/hatch)

-----
Python MCStatus is a library which wraps around the [mcstatus.io](https://mcstatus.io) API. It is developed very similar
to the [node-mcstatus](https://www.npmjs.com/package/node-mcstatus) npm package. It's essentially the same just ported to python.

**Table of Contents**

- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Installation

To install this package open your terminal for your workspace and use the following command:
```console
pip install python-mcstatus
```

## Usage
### Java Status
```python
from python_mcstatus import JavaStatusResponse, JavaServer

Server = JavaServer("demo.mcstatus.io", port=25565, query=True)   # port is optional and defaults to 25565

response: JavaStatusResponse = Server.get_status()
# You can receive an error in the above when the response is not 200, this copies the functionality from the node library.
```

### Bedrock Status
```python
from python_mcstatus import BedrockStatusResponse, statusBedrock

Server = BedrockServer('demo.mcstatus.io', port=19132)   # port argument is optional and defaults to 19132

response: BedrockStatusResponse = Server.get_status()
```


## License

`python-mcstatus` is distributed under the terms of the [MIT](https://spdx.org/licenses/MIT.html) license.
