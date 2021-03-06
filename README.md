ADXL345
=======

Python module to use ADXL345. Compatible with Python 2 and Python 3.

Based on [pimoroni/adxl345-python](https://github.com/pimoroni/adxl345-python).


## Install

Install it as a dependency using pip:

``` bash
pip install adxl345
```


## Usage

- Import module and instantiate an ADXL345

``` python
from adxl345 import ADXL345


adxl345 = ADXL345()
```

- Get 3-axis accelerations in m.s-²

``` python
axes = adxl345.get_axes()

# Returns something like:
# axes['x'] => -0.1614
# axes['y'] =>  0.0691
# axes['z'] =>  9.8064
```

- Get 3-axis accelerations in g (Earth gravity)

``` python
axes = adxl345.get_axes(True)

# Returns something like:
# axes['x'] => -0.0014
# axes['y'] =>  0.0001
# axes['z'] =>  1.0012
```

- Use another IC2 address

By default, this library uses the `0x53` I2C address.

To use another address, set it when creating an instance of ADXL345:

``` python
adxl345 = ADXL345(0x1D)
```


## Full example

``` python
from adxl345 import ADXL345


adxl345 = ADXL345()

axes = adxl345.get_axes(True)

# Returns something like:
# axes['x'] => -0.0014
# axes['y'] =>  0.0001
# axes['z'] =>  1.0012
```


## License

This project is under [MIT](LICENSE) license.
