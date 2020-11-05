# Ecganncompare

The program is used to compare annotation files obtained as a result of processing a set of ECG records. 
Annotation to databases are available on [ecg.ru](https://ecg.ru/).

## Resources

Professional tool for physicians and biomedical engineers  
https://ecg.ru/

## Documentation and examples

See the input and output [`format description`](./formats.md).

See file [`usage.md`](./usage.md) for an example of using the comparison results.

## Usage

Python (2.6 or later) must be installed on the user's computer to run the program.
The program accepts two JSON annotation files.
The launch is carried out through the command line.
Two arguments must be passed to the file `ecganncmp.py` as follows

    python ecganncmp.py ref_path test_path

- `ref_path` is a path to file with reference annotations or folder with these files,
- `test_path` is a path to file (or folder) with annotations, that need to be compare with reference,
- _both paths must point either to files or folders._

As a result of the program's work, a report is generated in JSON format.
By default, the report is output to the console window.
To output the report to a file, the `ecganncmp` program must be run as follows (in Windows OS)

    python ecganncmp.py ref_path test_path > output_filename

- `output_filename` is a path to file that will be contain report of annotation comparing.
