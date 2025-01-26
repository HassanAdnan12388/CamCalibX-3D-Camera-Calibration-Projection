# CamCalibX-3D-Camera-Calibration-Projection


## **Project Overview**
This project involves determining the **camera matrix** of a mobile phone camera by analyzing a 3D object captured in an image. The process requires marking at least 20 image points, defining their corresponding real-world coordinates in millimeters, and using these points to calculate the camera matrix.

---

## **Summary**
### **Objective**
- Capture an image of a **nonplanar 3D object** (e.g., a box).
- Mark and map **image coordinates** to their **real-world counterparts**.
- Calculate the **camera matrix** \( P \) using the gathered data.

### **Tasks**
1. **Defining Axes:** Label and visualize the X, Y, Z axes on the object.
2. **Marking Points:** Identify at least 20 image points using the `point_reader()` function.
3. **Coordinate Mapping:** Map image coordinates to real-world 3D coordinates.
4. **Camera Matrix Calculation:** Use the corresponding coordinates to compute the projection matrix.

---

## **Technologies Used**
- **Python Libraries:**
  - **NumPy**: For numerical operations and data structures.
  - **OpenCV**: For image processing and point marking.
  - **Matplotlib**: For visualization and plotting.
- **Camera Calibration Techniques**:
  - Manual marking of image points.
  - Transformation between 2D image space and 3D real-world space.

---

## **Architecture**
1. **Input Stage:**
   - Import image of a 3D object.
   - Define and visualize the X, Y, Z axes on the object.

2. **Data Collection:**
   - Use the `point_reader()` function to manually mark points on the image.
   - Map these points to real-world coordinates based on the physical dimensions of the object.

3. **Processing:**
   - Calculate the camera matrix \( P \) using the **Direct Linear Transformation (DLT)** or similar techniques.
   - Use the relationship \( s \cdot \textbf{x} = P \cdot \textbf{X} \), where:
     - \( \textbf{x} \) = Image point in homogeneous coordinates.
     - \( \textbf{X} \) = Real-world point in homogeneous coordinates.
     - \( P \) = Camera matrix.

4. **Output:**
   - Visualize the results with marked points and axes.
   - Output the calculated camera matrix.

---

## **Key Features**
- **Interactive Point Selection**: Mark points dynamically using the OpenCV GUI.
- **Customizable Coordinate System**: Define world coordinates based on the object's real-world layout.
- **Real-World Application**: Demonstrates essential concepts of camera calibration and projective geometry.

---
