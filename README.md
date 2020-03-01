# Coding challenge for AgBlox:

The 3 calculators calculate the line of best fit for the inputted data points.
The 3 generators try to generate points similar to the input.

## Dependencies

numpy, tensorflow, keras, random

## Usage

Use calc_lsr.py or calc_ml.py for best performance.
Older calculators and generators can be found in the "old" folder.

Enter the name of csv input file when prompted:
```bash
Enter the name of the file with points: 
```

The program will then run and will output generated data in the name entered for the input file preceded by "gen_"

## Modifications

If you would like to experiment with other generators, uncomment the generator you would like to use and comment out the current one.
```python
import gen_partition as gen
#import gen_distribution as gen
#import gen_kdf as gen

def get_file():
    (...)
    #uncomment to use resampling to generate points
    genx, geny = gen.generator(xs, slope, intercept, errors, len(xs))

    #uncomment to use a distribution to generate points
    #genx, geny  = gen.generator(xs, slope, intercept, errors, sd, len(xs))

    #uncomment to use kernel desnity to generate points
    #genx, geny = gen.generator(xs, ys, len(xs))
```
Note: make sure the calculator and generator are in the same folder.

## Author

Edward Zhou
