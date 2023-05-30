# pytone
A minimalist implementation of a vocal autotuner in Python, with no external dependencies except for Numpy.

### Quick Start
```
import pytone
pytone.tune("examples/original.wav", "examples/Dpentatonic.wav", "D", "pentatonic")
```

That's all there is to it. All twelve notes in the Western chromatic scale are supported, and can be referenced through any valid enharmonic notation (e.g. "F" is the same as "E#") excluding double sharps and double flats. A number can also be passed in place of the key letter for more precise tuning control:

```
pytone.tune("input.wav", "tuned.wav", 442, "major")
```

Valid arguments for the scale are **major**, **minor**, **chromatic**, and **pentatonic**.

To produce a diagram showing the original and output pitches, set the 'debug' argument to True:
```
pytone.tune("examples/original.wav", "examples/Dpentatonic.wav", "D", "pentatonic", debug=True)
```

Examples of tuned samples can be found in /examples.