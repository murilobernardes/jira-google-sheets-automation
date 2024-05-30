# Jira Google Sheets Automation

This project automates the process of extracting data from Jira and populating it into Google Sheets. It aims to simplify tracking and reporting by seamlessly integrating Jira issue data with Google Sheets.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)


## Introduction

This Python script automates data extraction from Jira and updates a Google Sheet with the latest information. It's useful for teams who need to keep track of their issues and want an easy way to generate reports or dashboards using Google Sheets.

## Features

- Connects to Jira and Google Sheets via their respective APIs.
- Extracts issues data from Jira.
- Updates Google Sheets with the extracted data.
- Customizable configurations for specific Jira queries and Google Sheets.

## Requirements

- Python 3.x
- [Jira Python Library](https://jira.readthedocs.io/)
- [Google API Python Client](https://developers.google.com/api-client-library/python/)

## Installation

1. Clone this repository:
    ```sh
    git clone https://github.com/yourusername/jira-google-sheets-automation.git
    cd jira-google-sheets-automation

2. Create and activate a virtual environment:

    ```sh 
    python -m venv venv
    .\venv\Scripts\activate

3. Install the required dependencies:

    ```sh
    pip install -r requirements.txt

4. Create an environment variables file (env_vars.sh) in the project directory with the following content, replacing the placeholders with your actual data:

    ```sh

    # JIRA API URL
    export JIRA_URL="https://your_jira_instance.atlassian.net/rest/api/2/search"

    # JIRA API Token
    export JIRA_TOKEN="your_jira_api_token"

    # JIRA JQL query
    export JQL="your_jira_query"  # Example: resolutionDate >= startOfDay(-90) AND resolutionDate <= endOfDay(-1)

    # Slack Webhook URL
    export SLACK_WEBHOOK_URL="your_slack_webhook_url"

    # Google Sheets ID
    export SHEET_ID="your_google_sheet_id"

    # Google Sheets Worksheet Name
    export SHEET_NAME="your_worksheet_name"

    # Path to Google API Credentials File
    export CREDENTIALS_FILE="path/to/your/service_account.json"

5. Load the environment variables:

   ```python

from dotenv import load_dotenv
load_dotenv('path/to/your/env_vars.sh')

## Usage
Configure the Jira and Google Sheets API credentials as described in the Configuration section.

Run the script:

   ```sh
    python script.py


## Configuration

To configure the script, you need to set up your environment variables in a file named env_vars.sh located in the project directory. Below are the required environment variables:

   ```sh
 
    # JIRA API URL
    export JIRA_URL="https://your_jira_instance.atlassian.net/rest/api/2/search"

    # JIRA API Token
    export JIRA_TOKEN="your_jira_api_token"

    # JIRA JQL query
    export JQL="your_jira_query"  # Example: resolutionDate >= startOfDay(-90) AND resolutionDate <= endOfDay(-1)

    # Slack Webhook URL
    export SLACK_WEBHOOK_URL="your_slack_webhook_url"

    # Google Sheets ID
    export SHEET_ID="your_google_sheet_id"

    # Google Sheets Worksheet Name
    export SHEET_NAME="your_worksheet_name"

    # Path to Google API Credentials File
    export CREDENTIALS_FILE="path/to/your/service_account.json"

Ensure you have all the necessary values in your env_vars.sh file before running the script.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your changes. For major changes, please open an issue first to discuss what you would like to change.



This `README.md` file provides a comprehensive overview of your project, including installation instructions, configuration details, and usage guidelines. It ensures that other users can easily understand and set up the project.



