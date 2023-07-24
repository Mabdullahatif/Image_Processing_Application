# Image Processing Mini-Project

This repository contains a C++ program for image processing operations on PGM (Portable Graymap) image files. The program allows users to load and save images, create negative images, apply mean and median filters, flip images horizontally and vertically, rotate images, resize images, and crop images.

## Table of Contents
- [Features](#features)
- [Description](#description)
- [How to Use](#how-to-use)
- [Contributing](#contributing)
- [License](#license)

## Features

- Load and save PGM image files.
- Create the negative of an image.
- Apply mean and median filters to an image.
- Flip images horizontally and vertically.
- Rotate images clockwise and counter-clockwise.
- Rotate images by an arbitrary angle.
- Resize images to custom dimensions.
- Crop images by specifying left, top, right, and bottom lengths.

## Description

The provided C++ code is an image processing application that operates on PGM (Portable Graymap) image files. It allows users to load, manipulate, and save images, as well as apply various image processing techniques. The program includes the following key components and functionalities:

1. **Libraries and Namespaces:**
   - The code includes several standard libraries: `<iostream>`, `<fstream>`, and `<vector>`. The `using namespace std;` statement allows the use of standard functions and objects without specifying the `std::` prefix.

2. **Struct PGMImage:**
   - This structure represents a PGM image. It contains members to store image properties, such as height (`H`), width (`W`), maximum gray value (`MaxGray`), and a 2D vector (`ImageData`) to store the pixel values of the image.
   - The constructor `PGMImage()` initializes the image properties to -1.
   - The function `Create()` is used to create a 2D vector for image data with a specified height and width.
   - The function `ReserveMemory()` allocates memory for the image based on the provided height and width.

3. **Image Loading and Saving:**
   - The functions `LoadImage()` and `SaveImage()` handle the loading and saving of PGM image files, respectively. The images are stored in a 2D vector (`ImageData`) within the `PGMImage` structure.
   - The `LoadImage()` function reads image data from a PGM file and allocates memory for the image.
   - The `SaveImage()` function writes the image data to a new PGM file.

4. **Image Manipulation Functions:**
   - `Create_Negative()`: This function creates the negative of the loaded image by subtracting each pixel value from the maximum gray value.
   - `Mean_Filter(FilterSize)`: Applies a mean filter to the image using a specified filter size (default is 3x3). It calculates the average of the pixel values within the filter window and replaces the central pixel with this average value.
   - `Median_Filter(FilterSize)`: Applies a median filter to the image using a specified filter size (default is 3x3). It calculates the median value of the pixel values within the filter window and replaces the central pixel with this median value.

5. **Image Transformation Functions:**
   - `Rotate(angle)`: Rotates the image by an arbitrary angle (in degrees) using bilinear interpolation to compute the pixel values of the rotated image.
   - `RotateClockwise()`: Rotates the image clockwise by 90 degrees.
   - `RotateCounterClockwise()`: Rotates the image counter-clockwise by 90 degrees.
   - `FlipHorizontal()`: Flips the image horizontally by exchanging pixel values between left and right columns.
   - `FlipVertical()`: Flips the image vertically by exchanging pixel values between top and bottom rows.

6. **Image Resizing and Cropping:**
   - `Resize(NewH, NewW)`: Resizes the image to the specified height and width using the nearest-neighbor interpolation method.
   - `CropImage(Left, Top, Right, Bottom)`: Crops the image by removing the specified number of rows and columns from the left, top, right, and bottom edges, respectively.

7. **Menu and User Interaction:**
   - The `Menu()` function displays a menu to the user, allowing them to choose from various image processing operations.
   - The `main()` function presents a loop that repeatedly displays the menu, processes user input, and executes the selected operation on the loaded image or the result of the previous operation.
   - Users can interact with the program by providing inputs such as file names, filter sizes, angles, etc., as required for specific operations.

The code provides a comprehensive set of image processing operations, enabling users to load, manipulate, and save images with ease. It covers various transformation and filtering techniques commonly used in basic image processing applications. Users can perform multiple operations sequentially on the same image, as well as save the final processed image to a new file.

## How to Use

1. **Clone or Download:** Clone or download the repository to your local machine using the "Code" button or Git command: `git clone https://github.com/your-username/image-processing-mini-project.git`
2. **Compile the Program:** Navigate to the project directory and compile the C++ program with a C++ compiler, e.g., `g++ -o image_processing main.cpp`
3. **Launch the Application:** Run the executable to launch the image processing application: `./image_processing`
4. **Choose an Operation:** Select an operation from the user-friendly menu, such as loading, saving, flipping, rotating, resizing, etc.
5. **Provide Inputs:** Follow the prompts to provide inputs like file names, angles, filter sizes, etc., as needed for the chosen operation.
6. **Execute the Operation:** The program will process the selected operation on the loaded image or the previous result.
7. **Continued Exploration:** Experiment with multiple operations on the same image or try different images for various transformations.
8. **Exit the Application:** To exit, select option 14 from the menu. Rerun the app to try new operations or process other images.

With these steps, you'll be able to effortlessly harness the power of image processing and explore the exciting possibilities of manipulating digital images using this C++ application.

## Contributing

Contributions to this project are welcome! If you have any suggestions, bug fixes, or new features to add, please open an issue or submit a pull request.

## Intial Contributor

So far, all the work in this repository is purely done by me and [Avcton](https://github.com/avcton)

