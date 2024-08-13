## Reach the site [here](https://erayyap.github.io/logprobs-viewer/index.html)

LogProb Viewer is a simple, interactive web application that allows users to visualize and explore token-level log probabilities from language model outputs. It provides an intuitive interface for parsing JSON data containing logprobs and displaying them in a user-friendly format.

## Features

- Parse and display JSON data containing token-level log probabilities
- Interactive token display with hover functionality
- Show main log probability and alternative tokens on hover
- Detailed information view on token click
- Responsive design for various screen sizes

## Installation

1. Clone this repository or download the HTML file:

   ```
   git clone https://github.com/yourusername/logprob-viewer.git
   ```

   or download the `index.html` file directly.

2. No additional installation is required as this is a standalone HTML file with embedded JavaScript and CSS.

## Usage

1. Open the `index.html` file in a modern web browser.

2. Paste your JSON data into the textarea. Make sure the JSON you are posting is in OpenAI API style.
Make sure you have the token probabilities enabled. For example in OpenAI completions API add the argument logprobs = true. 
The JSON should have the following structure:

   ```json
   {
     "choices": [
       {
         "message": {
           "content": "Your text content here"
         },
         "logprobs": {
           "content": [
             {
               "token": "token1",
               "logprob": -1.23,
               "bytes": [98, 121, 116, 101, 115],
               "top_logprobs": [
                 {"token": "token1", "logprob": -1.23},
                 {"token": "alternative1", "logprob": -2.34},
                 {"token": "alternative2", "logprob": -3.45}
               ]
             },
             // ... more tokens ...
           ]
         }
       }
     ]
   }
   ```

3. Click the "Process" button to parse and display the data.

4. Interact with the displayed tokens:
   - Hover over a token to see its log probability and alternative tokens.
   - Click on a token to view detailed information in the info box below.

## Contributing

Contributions to improve LogProb Viewer are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

If you have any questions or suggestions, please open an issue in this repository.