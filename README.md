# Pet Classifier Project

## Overview
The Pet Classifier project is a machine learning application designed to classify images of pets and other animals. It uses pre-trained models to identify whether an image contains a dog, cat, or other animals, and further classifies the breed of the pet if applicable. This project is ideal for learning about image classification, data preprocessing, and model evaluation.

## Project Structure
```
/workspaces/Machine-Learning-on-AWS
├── batch/
│   ├── run_models_batch_uploaded.sh  # Script to run models in batch mode for uploaded images
│   └── run_models_batch.sh           # Script to run models in batch mode
├── data/
│   ├── dognames.txt                  # List of dog breed names
│   ├── imagenet1000_clsid_to_human.txt # Mapping of ImageNet class IDs to human-readable labels
│   └── pet_images/                   # Directory containing pet and other animal images
│       ├── Basenji_00963.jpg
│       ├── Basenji_00974.jpg
│       ├── Basset_hound_01034.jpg
│       ├── Beagle_01125.jpg
│       ├── ...                       # Additional pet and animal images
├── hints/
│   ├── adjust_results4_isadog_hints.py
│   ├── calculates_results_stats_hints.py
│   ├── classify_images_hints.py
│   ├── get_input_args_hints.py
│   ├── get_pet_labels_hints.py
│   └── print_results_hints.py
├── scripts/
│   ├── __init__.py                   # Initialization file for the scripts module
│   ├── adjust_results4_isadog.py     # Adjusts classification results to identify dogs
│   ├── calculates_results_stats.py   # Calculates statistics for classification results
│   ├── check_images.py               # Main script to classify images
│   ├── classifier.py                 # Contains the classifier logic
│   ├── classify_images.py            # Classifies images using a pre-trained model
│   ├── get_input_args.py             # Parses command-line arguments
│   ├── get_pet_labels.py             # Extracts pet labels from image filenames
│   ├── print_functions_for_lab_checks.py # Utility functions for debugging
│   ├── print_results.py              # Prints classification results
│   └── __pycache__/                  # Compiled Python files
├── tests/
│   └── test_classifier.py            # Unit tests for the classifier
├── check_images.txt                  # Example output file for image classification
├── pyproject.toml                    # Project configuration file
├── README.md                         # Project documentation
└── uv.lock                           # Lock file for dependencies
```

## Features
- Classifies images of pets and other animals.
- Identifies whether an image contains a dog and determines its breed.
- Supports batch processing of images.
- Provides detailed statistics on classification results.

## Requirements
- Python 3.12 or higher
- Required Python libraries are listed in `requirements.txt` (to be created).

## Setup
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Machine-Learning-on-AWS
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure the `data/pet_images/` directory contains the images you want to classify.

## Usage
### Classify Images
Run the main script to classify images:
```bash
python scripts/check_images.py --dir data/pet_images/ --arch resnet --dogfile data/dognames.txt
```
- `--dir`: Directory containing images to classify.
- `--arch`: Model architecture (e.g., `resnet`, `alexnet`, `vgg`).
- `--dogfile`: File containing dog breed names.

### Batch Processing
To classify images in batch mode, use the provided shell scripts:
```bash
bash batch/run_models_batch.sh
```

## Testing
Run unit tests to verify the functionality of the classifier:
```bash
pytest tests/test_classifier.py
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a detailed description of your changes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
- Pre-trained models are sourced from PyTorch and TensorFlow.
- ImageNet dataset for class labels.

## Contact
For questions or feedback, please contact [your-email@example.com].