# 🏛️ Neural Style Transfer: Reimagining the Taj Mahal

This project implements Neural Style Transfer (NST) using a pretrained VGG19 network in PyTorch.

The objective is to combine the architectural content of the Taj Mahal with the artistic style of a reference artwork to generate a stylized image.

---

## 🎯 Project Goal

Neural Style Transfer separates:

* **Content** → structure and layout of an image
* **Style** → textures, colors, and artistic patterns

The generated image preserves the content of the Taj Mahal while adopting the visual style of the artwork.

---

## 🧠 Methodology

The implementation follows the approach proposed by Gatys et al.

### Pipeline

1. Load Content and Style Images
2. Preprocess Images
3. Extract Features using VGG19
4. Compute Gram Matrices
5. Calculate Content Loss
6. Calculate Style Loss
7. Optimize Generated Image
8. Visualize Results

---

## 🏗️ Architecture

### Content Representation

* Layer: `conv4_2`

### Style Representation

* `conv1_1`
* `conv2_1`
* `conv3_1`
* `conv4_1`
* `conv5_1`

### Loss Function

Total Loss = Content Loss + Style Loss

The generated image is optimized directly using gradient descent while VGG19 remains frozen.

---

## 📊 Results

The model successfully:

* Preserved the architectural structure of the Taj Mahal
* Transferred textures and colors from the style image
* Demonstrated the separation of content and style representations
* | Content | Style | Generated |
|----------|----------|----------|
| ![](images/content.jpg) | ![](images/style.jpg) | ![](images/result.jpg) |

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Torchvision
* NumPy
* Matplotlib
* VGG19

---

## 🚀 Future Improvements

* Multiple style blending
* Higher-resolution generation
* Fast Neural Style Transfer
* Real-time inference networks

---

## 📚 References

* Gatys, Leon A., et al. "A Neural Algorithm of Artistic Style"
* PyTorch Documentation
* VGG19 Architecture
