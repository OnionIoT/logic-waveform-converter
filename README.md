# logic-waveform-converter
Convert waveforms exported by Saleae Logic into pulse files useable by fast-gpio

## Waveform Sample CSV to Pulse File

Convert waveform sample csv files into pulse files that can be used with `fast-gpio` with:

```
python samples2pulses.py <Waveform Sample CSV File>
```

Will output a file the same name as the waveform csv but with the extension, `.pulse`.

### Notes

* The last high-low pair in the pulse file will be `0,0` since `fast-gpio` interprets that as the stop signal
* If the last value in the waveform is a 0, the last pulse will have a low pulse with a width of 5000us.
