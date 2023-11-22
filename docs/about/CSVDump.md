## CSVDump.py

CSVDump.py is a Python script that converts a CSV file downloaded from
ODK Central to OpenStreetMap (OSM) XML format. The tool can be useful
for users who want to work with OpenStreetMap data and want to convert
ODK Central data into a compatible format.

    options:
     -h, --help                   - show this help message and exit
     -v, --verbose                - verbose output
     -i CSVFILE, --infile CSVFILE - Specifies the path and filename of the input CSV file downloaded from ODK Central. This option is required for the program to run.

### Examples

To convert a CSV file named "survey_data.csv" located in the current
working directory, the following command can be used:

    [path]/CSVDump.py -i survey_data.csv

To enable verbose output during the conversion process, the following
command can be used:

    [path]/CSVDump.py -i survey_data.csv -v

### Input Format

CSVDump.py expects an input file in CSV format downloaded from ODK
Central. The CSV file should have a header row with column names that
correspond to the survey questions. Each row in the CSV file should
contain a response to the survey questions, with each column
representing a different question.

### Output Format

The output of CSVDump.py is an OSM XML file that can be used with
OpenStreetMap data tools and services. The converted OSM XML file will
have tags for each survey question in the CSV file, as well as any
metadata associated with the survey. The format of the OSM XML file
generated by CSVDump.py is compatible with other OpenStreetMap data
tools and services.

### Limitations

- CSVDump.py only supports CSV files downloaded from ODK
  Central. Other CSV files may not be compatible with the tool.
- The tool only supports simple data types such as strings, numbers,
  and dates. Complex data types such as arrays and nested structures
  are not supported.