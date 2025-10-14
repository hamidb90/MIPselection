# MIP selection

Peak-centered MIP selection from ADC histograms. Input CSVs must have three columns without a header: time_ns, chan, ph.

## Install
```bash
python -m venv .venv && . .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install numpy pandas matplotlib scipy
```

## Use in Jupyter
Paste the single cell from the notebook and run. By default it auto-picks four CSV files in the current folder. To specify files explicitly, fill FILES at the top of the cell.

Outputs go to ./mip_outputs

## Method
Savitzky-Golay smoothing for the histogram, strict peak pick inside a muon ADC band, then MIP bounds by fractional-height crossings relative to a local baseline, with guard and minimum width.

## License
MIT
