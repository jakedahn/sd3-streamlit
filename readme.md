# SD3 Image Generator App

NOTE: This is a modified version of https://github.com/Doriandarko/sd3-streamlit from [@skirano](https://twitter.com/skirano) on twitter: https://twitter.com/skirano/status/1780690317714370836

Significant modifications were made by prompting the cursor.sh editor. The code is very not clean, but don't blame me, it was written by `gpt-4-turbo-2024-04-09`

---

This Streamlit application allows users to generate images using the Stability AI API. It supports both "text-to-image" and "image-to-image" modes, providing a user-friendly interface for creating images based on textual prompts or modifying existing images.

## Features

- **Text-to-Image**: Generate images from textual descriptions.
- **Image-to-Image**: Modify uploaded images based on textual prompts and selected strength settings.

## Installation

To run this application, you will need Python and several dependencies installed.

### Prerequisites

- Python 3.6 or higher
- pip

### Dependencies

Install the required Python packages using:

```bash
pip install requirements.txt
```

## Usage

First, you'll want to setup your environment variables, by copying the example file, then filling in your stabilityai api key.

```bash
cp .env.example .env
```

To start the application, navigate to the directory containing `app.py` and run the following command:

```bash
source .env
streamlit run app.py
```

The application will start and be accessible through a web browser at `http://localhost:8501`.

## Functionality

### Generating Images

1. **Text-to-Image**:

   - Enter a descriptive prompt.
   - Click "Generate Image".
   - View the generated image below the button.

2. **Image-to-Image**:
   - Upload an image.
   - Optionally adjust the strength slider to control the transformation intensity.
   - Enter a prompt describing the desired modifications.
   - Click "Generate Image".
   - View the modified image below the button.

### Output

Generated images are saved in the `./outputs` directory with a timestamp, model prefix, seed, as well as json files containing metadata about how each of the images were generated. This should make it easy to keep track of different sessions and models used.

## Contributing

Contributions to this project are welcome! Please fork the repository and submit a pull request with your proposed changes.

## License

This project is open-sourced under the MIT License. See the LICENSE file for more details.

## Acknowledgments

- Stability AI for providing the API used in this application.
- Streamlit for the framework that powers the web interface.
- https://github.com/Doriandarko/sd3-streamlit
