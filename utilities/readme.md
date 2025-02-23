<<<<<<< HEAD
- **utilities/**:
  - Example Project: A **JSON to CSV file converter** script with options to customize the CSV format.
  - Ideal Contributions: Add support for other file formats, include a GUI for easier use, or enhance error handling.
=======
Utilities Folder
This folder contains utility scripts that help in performing various tasks. Each utility is designed to be modular and extendable, allowing for easy integration into other projects.

File Structure
bash
utilities/
│
├── jsontocsv.js    # A script to convert JSON files into CSV format
├── input.json        # Sample input JSON file for conversion
└── README.md         # Documentation for the utilities
Utility Scripts
1. JSON to CSV Converter
The json-to-csv.js script converts a JSON file into CSV format. It provides options for customizing the output, such as specifying a delimiter and whether to include headers in the CSV file.

Features
Custom Delimiter: You can choose a delimiter for the CSV file (default is ,).
Headers: Includes the option to add or remove headers in the CSV output.
Error Handling: The script checks if the input JSON is an array of objects and handles errors gracefully.
Usage
Prerequisites
Node.js installed on your system.
Instructions
Place your input JSON file in the utilities/ folder and name it input.json or modify the script to point to the correct file path.
Run the script using Node.js.
bash

node jsontocsv.js
This will convert the JSON data from input.json into a CSV file (output.csv) in the same folder.

Options
You can customize the conversion by passing options to the convertJsonToCsv function:

Delimiter: Specify a custom delimiter (default is ,).
Headers: Choose whether to include headers in the CSV file (default is true).
Example of modifying options in the script:

javascript
Copy code
convertJsonToCsv(inputFile, outputFile, {
  delimiter: ";",     // Use semicolon as the delimiter
  includeHeaders: false,  // Skip headers in the output
});
Sample JSON Input (input.json)
json
Copy code
[
  {
    "name": "John Doe",
    "age": 28,
    "email": "john@example.com"
  },
  {
    "name": "Jane Doe",
    "age": 25,
    "email": "jane@example.com"
  }
]
Sample CSV Output (output.csv)
perl
Copy code
"name","age","email"
"John Doe",28,"john@example.com"
"Jane Doe",25,"jane@example.com"
Error Handling
The script will throw an error if:

The input file is not in the correct format (e.g., the JSON is not an array of objects).
The input file cannot be read due to permissions or path issues.

# JSON to CSV Converter (CLI Support)

The `json-to-csv.js` script now supports command-line interface (CLI) usage, allowing users to easily convert JSON files to CSV format via the terminal.

## Usage

```bash
node jsontocsv.js <inputFile> <outputFile> [options]
<inputFile>: The path to the JSON file that needs to be converted.
<outputFile>: The path where the CSV file will be saved.
[options]: Optional flags to customize the conversion process.
Available Options
--delimiter <delimiter>: Specifies a custom delimiter for the CSV file (default is ,).
--no-headers: Excludes headers (column names) from the CSV output.
>>>>>>> 6b4f976b66418ae46d4a60a5769d76d2641d812b
