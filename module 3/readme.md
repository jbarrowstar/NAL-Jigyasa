# Image Registration using Point Mapping

## Overview
The **Image Registration using Point Mapping** project implements an interactive **JavaScript-based solution** for aligning images using **Affine Transformation**. This method is widely used in **medical imaging, remote sensing, and computer vision** to correct image distortions and improve analysis accuracy.

---

## Objective
- Develop a **web-based tool** to align images using control points.
- Apply **Affine Transformation** to map input images onto reference images.
- Provide an interactive **GUI for selecting control points**.
- Enable **overlay visualization** for image comparison.

---

## Scientific Concepts Applied

### **1. Affine Transformation**
An **Affine Transformation** preserves **points, straight lines, and planes** while allowing **translation, rotation, scaling, and shearing**.

The transformation equation:

\[
\begin{bmatrix} X' \\ Y' \end{bmatrix} =
\begin{bmatrix} a & b \\ c & d \end{bmatrix} 
\begin{bmatrix} X \\ Y \end{bmatrix} + 
\begin{bmatrix} e \\ f \end{bmatrix}
\]

Where:
- \( (X, Y) \) are the original coordinates.
- \( (X', Y') \) are the transformed coordinates.
- \( a, b, c, d \) define rotation, scaling, and shearing.
- \( e, f \) define translation.

### **2. Control Point Selection**
- Users manually select **corresponding points** in both the base and input images.
- These points form a system of equations to compute the **Affine Transformation Matrix**.

### **3. Image Overlay with Transparency**
- The transformed image is overlaid onto the reference image.
- The **alpha transparency** property ensures proper visibility:

\[
I_{overlay} = \alpha \times I_{transformed} + (1 - \alpha) \times I_{reference}
\]

Where:
- \( \alpha \) controls transparency (0 = fully transparent, 1 = fully opaque).

---

## Significance
✅ **Accurate Image Alignment:** Useful in **remote sensing, medical imaging, and object detection**.  
✅ **Real-Time Visualization:** Users can interactively align images and **preview transformations**.  
✅ **Web-Based Processing:** No need for external tools like **MATLAB or OpenCV**.  
✅ **Customizable Overlay Transparency:** Allows better comparison between images.  

---

## Features
✅ **Manual Selection of Control Points**  
✅ **Computation of Affine Transformation Matrix**  
✅ **Live Overlay of Transformed Image**  
✅ **Adjustable Transparency for Comparison**  
✅ **Export Aligned Image**  

---

## Technologies Used
- **Frontend:** HTML, CSS, JavaScript  
- **Mathematical Models:** Affine Transformation, Matrix Computation  
- **Visualization:** Canvas API for Image Processing  

---

## Installation & Setup
### **Prerequisites**
Ensure you have the following installed:
- **Node.js** (for JavaScript-based processing tools)
- **Web Server** (Apache, Nginx, or VS Code Live Server extension)

### **Installation Steps**
```bash
# Clone the repository
git clone (https://github.com/jbarrowstar/NAL-Jigyasa.git)

# Navigate to the project directory
cd module3

# Open in browser (for static HTML/JS files)
```

---

## Contributing
We welcome contributions! To contribute:
1. Fork the repository.
2. Create a new branch (`feature-branch`).
3. Implement your changes and commit.
4. Open a Pull Request.

---

## License
This project is licensed under the **MIT License**.

---

## Contact & Support
For inquiries, reach out to **JB Arrowstar Solutions**:
📧 Email: info@jbas.co.in
🌐 Website: [JB Arrowstar Solutions](https://jbas.co.in)  
📍 Address: Bangalore, India  

---

## Acknowledgments
Special thanks to **NAL Jigyasa** for research contributions and project sponsorship. This project integrates **Affine Transformations, control point selection, and image alignment techniques** for next-gen image processing.
