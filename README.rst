GPIO\_Calculator
================

Simple GPIO calculator for libgpiod based on its chardev

Installation
------------

.. code::

    pip install git+https://github.com/yeyeto2788/GPIO_Calculator

Usage
-----

.. code::

    from gpio_calculator import Calculator

    calculator = Calculator()
    # Get chardev based on pin letter and pin number.
    # Return should be 242
    calculator.get_chardev("H", 18)
    # Get chardev from list.
    # Returns a list of converted items [242, 243,244].
    calculator.get_chardevs(["H18", "H19", "H29"])

    # Get pin from chardev.
    # Returns the pin number H18
    calculator.get_pin(242)
    # Get all pins from chardevs
    # Returns all pins found H18, H19, H20
    calculator.get_pins([242, 243, 244])

