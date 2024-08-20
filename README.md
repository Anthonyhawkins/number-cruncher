# Number Cruncher CLI Utility
This repo defines the requirements of a CLI utility which provides a number of math utilities.  A Unit Converter, Basic Calculator, and Area Calculator.



## Usage
Any implementation of the CLI should implement the following commands and options.
```text
CLI Tool: NumberCruncher

Usage:
  numcrunch [options]

Options:
  -command string
        The type of operation to perform. Valid commands are: length, weight, volume, temperature, time, speed, area, calc, areacalc.
  -from string
        The unit to convert from (only for unit conversions).
  -to string
        The unit to convert to (only for unit conversions).
  -value float64
        The value to convert or the first operand for calculator operations.
  -value2 float64
        The second operand for calculator operations (only for add, subtract, multiply, divide).
  -shape string
        The shape to calculate the area for. Valid shapes are: square, circle, triangle (only for areacalc).
  -side float64
        The side length for square area calculation (only for areacalc with shape=square).
  -radius float64
        The radius for circle area calculation (only for areacalc with shape=circle).
  -base float64
        The base length for triangle area calculation (only for areacalc with shape=triangle).
  -height float64
        The height for triangle area calculation (only for areacalc with shape=triangle).
  -h, --help
        Displays help information.
  -v, --version
        Displays the version of the CLI tool.

Supported Commands and Units:

  length:
    Supported units: inches, centimeters, feet, meters, miles, kilometers, yards, millimeters
    Example:
      numcrunch -command=length -from=inches -to=centimeters -value=10

  weight:
    Supported units: pounds, kilograms, ounces, grams, tons, metrictons, stone, milligrams
    Example:
      numcrunch -command=weight -from=pounds -to=kilograms -value=50

  volume:
    Supported units: gallons, liters, quarts, pints, cups, fluidounces, milliliters
    Example:
      numcrunch -command=volume -from=gallons -to=liters -value=3

  temperature:
    Supported units: celsius, fahrenheit, kelvin
    Example:
      numcrunch -command=temperature -from=celsius -to=fahrenheit -value=25

  time:
    Supported units: seconds, minutes, hours, days, weeks, months
    Example:
      numcrunch -command=time -from=hours -to=days -value=48

  speed:
    Supported units: mph, kmh, fps, mps, knots
    Example:
      numcrunch -command=speed -from=mph -to=kmh -value=60

  area (unit conversion):
    Supported units: squarefeet, squaremeters, acres, hectares, squareinches, squarecentimeters
    Example:
      numcrunch -command=area -from=squarefeet -to=squaremeters -value=500

  calc:
    Supported operations: add, subtract, multiply, divide
    Example:
      numcrunch -command=calc -from=add -value=10 -value2=5
      Performs 10 + 5 and outputs the result.

  areacalc:
    Calculates the area of a given shape.
    Supported shapes: square, circle, triangle

    Example:
      numcrunch -command=areacalc -shape=square -side=5
      Calculates the area of a square with side length 5.

      numcrunch -command=areacalc -shape=circle -radius=3
      Calculates the area of a circle with radius 3.

      numcrunch -command=areacalc -shape=triangle -base=4 -height=5
      Calculates the area of a triangle with base 4 and height 5.
```

## Testing Data
Included within `test-data.json` are known calculations which can be used for testing.