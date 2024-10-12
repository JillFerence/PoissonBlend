# PoissonBlend - Image Blending Tool

## Description
PoissonBlend is a Python-based tool designed to seamlessly blend a selected region from a source image into a target image, using Poisson blending with second-order derivatives and least square optimization. This technique is ideal for object insertion and image editing tasks, where smooth transitions between the blended images are crucial. Users can select a patch from the source image containing an object they wish to insert, and the tool will integrate it naturally into the target image.

### Technologies Used
- **Python**: The primary language used for developing the blending tool.
- **OpenCV**: Used for image processing and handling tasks such as reading and writing images.
- **NumPy**: Used for numerical operations and matrix manipulations.
- **Matplotlib**: Used for visualizing images before and after the blending process.
- **SciPy**: Utilized for solving the least squares optimization problem involved in the blending process.
- **Tkinter**: For building the graphical user interface (GUI) to allow users to select images.
- **Os**: For handling file paths and system directories, such as saving outputs to the Downloads folder.

### Features
- **Source and Target Image Blending:** Allows users to choose a region from the source image and blend it onto the target image seamlessly.
- **Boundary Smoothness:** Ensures the boundaries between the blended object and the target image appear natural by solving for gradients.
- **Support for Grayscale and Color Images:** Handles both types of images for flexibility in image editing.
- **Visualization:** Provides a comparison between the original images and the final blended result for easy verification.

Example of the blending process:
- Source Image Example:
  <br>![source1](https://github.com/user-attachments/assets/fc5fefd8-2fac-4e7c-88c6-bcd5ac0cd7ad)
- Target Image Example:
  <br>![target](https://github.com/user-attachments/assets/4ca06ea7-ef40-4466-8fa9-8fb9a1045cd9)
- Copy and Paste Image Example:
  <br>![copy_paste_image](https://github.com/user-attachments/assets/d932219e-63ef-412b-95bf-0bb60a02c6ad)
- Blended Image Example:
  <br>![blended_image](https://github.com/user-attachments/assets/706c7dbb-78ee-4b0d-93d3-27de25668200)
  
## Setup & Usage
To set up PoissonBlend, follow these steps:

1. **Prerequisites:**
    - Ensure you have Python 3.x installed.
    - Install required libraries by running the following command: pip install numpy opencv-python matplotlib scipy

2. **Clone the repository:**
    - Open your terminal and run the following command: git clone https://github.com/JillFerence/PoissonBlend.git

3. **Run the Blending Tool:**
    - Navigate to the project directory: cd PoissonBlend
    - Run the script to start the blending process: python main.py

4. **Select the Source and Target Images:**
    - The script will prompt you to select a source image and a target image from your local directory.

5. **Select the Region from the Source Image:**
    - Define the region to blend from the source image by selecting points around the desired patch to put onto the target image.

6. **Adjust the Position of the Selected Region on the Target Image:**
    - **R** key: Rotate the source by 10 degrees.
    - **S** key: Scale up the source image.
    - **A**: Scale down the source image.
    - **Up arrow** key: Move the source upward.
    - **Down arrow** key: Move the source downward.
    - **Left arrow** key: Move the source left.
    - **Right arrow** key: Move the source right.
    - **Q** key: Confirms the position and proceeds with blending.
  
7. **View the Blended Image**
    - After processing, the blended image will be saved to your Downloads folder.
    - A summary will be displayed using Matplotlib that includes a comparison visualization and least squared errors.
      
With these steps, you should be ready to start using the PoissonBlend tool!

## Sources
- Used for general logic and approach to Poisson blending
  <br>[erkaman.github.io/posts/poisson_blending.html](https://erkaman.github.io/posts/poisson_blending.html)
- Used for converting 2D coordinates to 1D indexing and processing each colour channel independently (R, G, B)
  <br>[/github.com/Erkaman/poisson_blend](https://github.com/Erkaman/poisson_blend)
- Used for setting A to be identity and b the value of the target image when the target mask and processing each colour channel independently (R, G, B)
  <br>[cs.brown.edu/courses/cs129/results/proj2/taox/](https://cs.brown.edu/courses/cs129/results/proj2/taox/)

## Credits
This project was completed for credit in CMPT 742 - Visual Computing Lab I at Simon Fraser University.
- **Developer**: Jill Ference  
  [GitHub Profile](https://github.com/jillference) | [LinkedIn](https://linkedin.com/in/jillference)
- Amir Alimohammadi for getting mask and aligning target base code
