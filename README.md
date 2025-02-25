# NLP--assignment-2# NLP-assignment-No.2

# Text Slicing with Cosine Distance

## Overview

This project, developed as part of the NLP course for a Master's degree in Artificial Intelligence at the University of Verona, involves the implementation of a text slicing algorithm based on cosine distance. The primary goal is to generate slices of input text while adhering to specified criteria, such as a context window size and an overlap threshold. The process includes text preprocessing, cosine distance calculation, and saving the generated slices to individual files.

## Features

- **Random Sentence Generation:** Utilizes the Faker library to generate random sentences for creating a dummy text file.

- **Dummy Text File Creation:** Creates a dummy text file with a specified size by repeatedly appending random sentences until the target size is reached.

- **Text Preprocessing:** Tokenizes, removes stopwords, and performs stemming on the input text.

- **Cosine Distance Calculation:** Calculates the cosine distance between two input texts after preprocessing.

- **Text Slicing:** Generates slices of input text based on a specified context window size and overlap threshold. The slicing process considers cosine distance to ensure slices are distinct.

- **Saving Slices to Files:** Saves the generated slices to individual files in a specified output directory.

## Usage

1. Adjust the parameters such as `file_size_mb`, `context_window_size_mb`, and `overlap_threshold` as needed in the script.

2. Run the script to create a dummy text file, generate slices, and save them to files.

```python
# Example usage
file_path = '/path/to/dummy_file.txt'
output_directory = '/path/to/slices_output'
file_size_mb = 350

create_dummy_text_file(file_path, file_size_mb)

with open(file_path, 'r', encoding='utf-8') as file:
    input_text = file.read()

slices = generate_slices(input_text)
print("\nNumber of slices:", len(slices))
print("\nSlices:")
for i, slice_text in enumerate(slices):
    print(f"Slice {i + 1} - Size: {len(slice_text)} bytes")

save_slices_to_files(slices, output_directory)
```

## Requirements

- Python 3.x
- Required Python packages: nltk, scikit-learn, faker

## License

This project is licensed under the [MIT License](LICENSE).

---
