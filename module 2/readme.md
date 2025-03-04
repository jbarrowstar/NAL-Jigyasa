# Synthetic Aerial Image Generation

## Overview
The **Synthetic Aerial Image Generation** project provides a **GUI-based tool** for processing and transforming aerial images using advanced **3D transformations**. It enables **realistic image analysis** through the application of camera **intrinsic and extrinsic parameters**.

---

## Objective
- Develop a **GUI tool** to generate synthetic aerial images.
- Implement **coordinate transformations** to convert image pixels into real-world coordinates.
- Support **TIFF image uploads** and **3D rendering**.
- Provide **adjustable camera parameters** for precise analysis.

---

## Scientific Concepts Applied

### **1. Coordinate Frames & Transformations**
The project involves multiple coordinate reference frames for accurate image projection:

- **Inertial Frame (Earth-Fixed):** \( (X_i, Y_i, Z_i) \) - A global reference frame fixed to Earth.
- **Gimbal Frame:** \( (X_g, Y_g, Z_g) \) - Originates at the center of gimbal rotation, with \( Z_g \) pointing along the optical axis.
- **Camera Frame:** \( (X_c, Y_c, Z_c) \) - Centered at the camera's optical center.
- **Image Frame:** Defined in **pixels** and **meters**, measured from the camera's principal point.

#### **Transformations:**
- **Inertial to Gimbal Frame Transformation:**

\[
 R_g = \begin{bmatrix} 
 \cos \beta & 0 & \sin \beta \\
 0 & 1 & 0 \\
 -\sin \beta & 0 & \cos \beta 
 \end{bmatrix} 
 \times 
 \begin{bmatrix} 
 1 & 0 & 0 \\
 0 & \cos \alpha & -\sin \alpha \\
 0 & \sin \alpha & \cos \alpha 
 \end{bmatrix}
\]

- **Gimbal to Camera Frame Transformation:**

\[
 R_c = \begin{bmatrix} 
 0 & -1 & 0 \\
 0 & 0 & -1 \\
 1 & 0 & 0 
 \end{bmatrix} 
\]

### **2. Camera Projection Model**
A **perspective camera** projects a 3D object point \( p_{obj} = [p_x, p_y, p_z, 1]^T \) onto a 2D image point \( q = [x_{ip}, y_{ip}, 1]^T \) using the relation:

\[
 x_{ip} = \frac{f \cdot p_x}{p_z}, \quad y_{ip} = \frac{f \cdot p_y}{p_z} 
\]

Where:
- \( f \) is the **focal length** of the camera.
- \( C \) is the **camera calibration matrix**.
- \( A \) is the **depth-dependent scaling matrix**.

### **3. Pixel to World Coordinate Transformation**
To determine the **real-world coordinate** corresponding to an image pixel:

\[
 P_{world} = R_{camera}^{-1} \times (K^{-1} \times P_{image})
\]

Where:
- \( K \) is the **camera matrix**.
- \( R_{camera} \) is the **camera rotation matrix**.

---

## Significance
✅ **Enhanced Image Analysis:** Allows manipulation of aerial images with high precision.  
✅ **Educational Value:** Provides insights into photogrammetry and **3D image transformations**.  
✅ **Real-World Applications:** Used in **geospatial analysis, urban planning, and defense applications**.  
✅ **Customizable UI:** Users can modify **camera parameters** to simulate real-world imaging.  

---

## Features
✅ **TIFF File Upload & Processing**  
✅ **Adjustable Camera Intrinsic Parameters** (Focal Length, Pixel Size, Image Dimensions)  
✅ **Adjustable Camera Extrinsic Parameters** (Latitude, Longitude, Altitude, Pan, Tilt)  
✅ **3D Rendering with WebGL & Three.js**  
✅ **Export Processed Images**  

---

## Technologies Used
- **Frontend:** HTML, CSS, JavaScript  
- **Libraries:** Three.js, TIFF.js  
- **Rendering Engine:** WebGL-based Image Visualization  

---

## Installation & Setup
### **Prerequisites**
Ensure you have the following installed:
- **Node.js** (for JavaScript-based processing tools)
- **Web Server** (Apache, Nginx, or VS Code Live Server extension)

### **Installation Steps**
```bash
# Clone the repository
git clone https://github.com/jbarrowstar/NAL-Jigyasa.git
# Navigate to the project directory
cd module2

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
🌐 Website: [JB Arrowstar Solutions](https://jbarrowstarsolutions.com)  
📍 Address: Bangalore, India  

---

## Acknowledgments
Special thanks to **NAL Jigyasa** for research contributions and project sponsorship. This project integrates **3D transformations, geospatial analysis, and image processing technologies** for next-gen synthetic aerial image generation.
