{% embed url="https://www.youtube.com/watch?v=Kv1Hiv3ox8I" %}

## What is JPEG?
JPEG (Joint Photographic Experts Group) is a widely used image file format that utilizes **lossy compression** to reduce file sizes. It is commonly used for digital photographs and web graphics where smaller file size is preferred over perfect image quality.

### Key Features:
- **Compression**: JPEG uses lossy compression, meaning some image data is lost to make the file size smaller. 
- **File Extension**: `.jpeg` or `.jpg` 
- **Usage**: Ideal for photos, complex images, and online sharing, but not suitable for graphics with sharp edges or text-heavy images.

## How JPEG Works?
JPEG works by compressing images through a process of **lossy compression**, which reduces file size by selectively discarding some of the image data. Here's a step-by-step breakdown of how JPEG compression works:

### 1. Color Space Conversion
The image is converted from **RGB** (Red, Green, Blue) to **YCbCr**, where:
- **Y** represents brightness (luminance). 
- **Cb** and **Cr** represent color information (chrominance). 
- Human eyes are more sensitive to changes in brightness than color, so color data can be compressed more heavily.

### 2. Downsampling
- The chrominance channels (**Cb** and **Cr**) are downsampled, meaning their resolution is reduced since the human eye is less sensitive to small changes in color.

### 3. Discrete Cosine Transform (DCT)
- The image is divided into **8x8 pixel blocks**. 
- Each block is transformed using the **Discrete Cosine Transform (DCT)**, which turns the image data into a sum of cosine waves at different frequencies. 
- This allows the JPEG algorithm to represent the image with fewer data points.

### 4. Quantization
- The DCT coefficients are **quantized**, meaning they are rounded to reduce precision. This is where most of the image data loss occurs. 
- Higher frequency details (small or subtle changes) are reduced, while lower frequency details (large or prominent features) are preserved. 
- The extent of quantization depends on the **compression level** chosen (higher compression results in lower quality).

### 5. Entropy Encoding
- The quantized data is then compressed using **entropy encoding techniques** such as **Huffman coding** or **Arithmetic coding**. 
- These techniques further compress the data by representing more common values with shorter codes.

### 6. Reconstruction
- When the image is opened, the process is reversed: the compressed data is decoded and converted back to pixel values.
- However, some detail lost during quantization cannot be restored, hence the "lossy" nature of JPEG.

### Pros & Cons of This Process:
- **Pros**: 
	- Greatly reduces file size for photos and complex images. 
	- Suitable for web usage and storage. 
- **Cons**: 
	- Lose of image quality, especially after multiple saves. 
	- Not ideal for images with sharp edges or text (introduces artifacts like blurring.)