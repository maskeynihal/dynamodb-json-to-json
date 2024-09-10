# DynamoDB JSON to JSON Converter

This simple web-based application allows you to convert DynamoDB JSON to regular JSON and vice versa. It provides a user-friendly interface to marshal or unmarshal DynamoDB JSON and copy the results for further use.

## Features

- **Unmarshall DynamoDB JSON**: Convert DynamoDB JSON format into a regular JSON structure.
- **Marshall JSON**: Convert regular JSON back into DynamoDB JSON format.
- **Copy to Clipboard**: Easily copy the results of both DynamoDB and regular JSON with a button click.

## Technologies Used

- **HTML**: Provides the structure of the page.
- **CSS**: Styles the page for a clean and simple UI.
- **JavaScript**: Handles the logic for converting JSON and interacting with AWS DynamoDB SDK.
- **AWS SDK for JavaScript**: Leverages the AWS SDK to marshall and unmarshall DynamoDB JSON.

## How to Use

1. Enter DynamoDB JSON in the left textarea box.
2. Click the **"Unmarshall to JSON"** button to convert it into regular JSON.
3. Enter regular JSON in the right textarea box.
4. Click the **"Marshall to DynamoDB JSON"** button to convert it back to DynamoDB JSON.
5. Use the **"Copy to Clipboard"** buttons to easily copy the content from either text area.

## Code Explanation

- **HTML Structure**:  
  The application consists of two containers, each with a textarea for input/output and buttons for marshalling/unmarshalling and copying.
- **CSS Styling**:  
  The CSS ensures a minimalistic and responsive design with a clean layout, button hover effects, and shadow boxes for better UX.

- **JavaScript Functionality**:  
  JavaScript functions handle the conversion between DynamoDB JSON and regular JSON using AWS SDK's `AWS.DynamoDB.Converter` functions.

  - `unmarshall()`: Converts DynamoDB JSON to regular JSON.
  - `marshall()`: Converts regular JSON to DynamoDB JSON.
  - `copyToClipboard()`: Copies the content of a specified textarea to the clipboard.

## Prerequisites

- The application uses **AWS SDK** for marshalling and unmarshalling, which is loaded via a CDN:

  ```html
  <script
    src="https://cdnjs.cloudflare.com/ajax/libs/aws-sdk/2.422.0/aws-sdk.min.js"
    integrity="sha256-Da7C+cls1rahhFZCYIqCtpuiTu3Q3OYo2z8H7i394Ss="
    crossorigin="anonymous"
  ></script>
  ```

### Responsive Design

The page layout adapts to different screen sizes, ensuring usability across devices.
