# Euro-Converter-Api
Description
Python application that converts Euros (EUR) to US Dollars (USD), British Pounds (GBP), or Japanese Yen (JPY) using real-time exchange rates fetched from the Frankfurter API. The application features an interactive menu and keeps track of your conversion history during the active session.

Features
Live Exchange Rates: Retrieves up-to-date conversion rates upon startup via a REST API.

Multiple Currencies: Convert from EUR to USD, GBP, or JPY.

Session History: View a chronological log of all conversions made during the current execution.

Interactive Menu: Easy-to-use numbered menu interface for seamless navigation.

Input Validation: Includes error handling to catch non-numeric inputs and prevent application crashes.

Prerequisites
Python 3.10 or higher: Required due to the use of structural pattern matching (match-case statements).

Requests Library: Used for handling HTTP requests to the API.

Installation
Clone this repository to your local machine.

Install the required dependencies using pip:

Bash
pip install requests
Usage
Navigate to the directory containing the script and run it via the terminal:

Bash
python file_name.py
(Note: Replace file_name.py with the actual name of your Python file).

Upon execution, you will be presented with the following interactive menu:

1: Convert to US Dollars (USD)

2: Convert to British Pounds (GBP)

3: Convert to Japanese Yen (JPY)

4: View Conversion History

5: Exit the program

Select your desired option by entering the corresponding number. If you choose to convert a currency, the program will prompt you to input the amount in Euros and will instantly display the calculated result.

Under the Hood
Data Fetching: The script sends a single GET request to [https://api.frankfurter.app/latest?from=EUR](https://api.frankfurter.app/latest?from=EUR) when launched, storing the JSON response in a dictionary for rapid calculations.

Memory Management: The conversion history is stored in a standard Python list. Please note that this data is session-bound and will be cleared once the program is closed.
