# LSB Image Steganography

LSB Image Steganography is a project for securely hiding (“encoding”) secret messages or files inside images using Least Significant Bit (LSB) manipulation. This technique ensures that changes are visually undetectable while providing a robust way to conceal information.

---

## 🚀 Features

- Encode secret text or files within BMP images.
- Supports decoding to recover original hidden information.
- Preserves original image appearance—no visible quality loss.
- Works with **.bmp** (bitmap) images for maximum compatibility and security.
- Command-line interface for seamless integration and automation.
- Error handling for invalid input files, capacity overflow, and format checks.

---

## 🖼️ How It Works

- **Encoding:**  
  Secret data is embedded into the least significant bits (LSBs) of the image’s pixel data. The result is a “stego image” that looks and behaves like the original but contains hidden data.

- **Decoding:**  
  The program extracts the concealed data by reading the LSBs in the encoded image and reconstructs the original secret message or file.

---

## 💻 Usage

### Command-Line Examples

#### Encode
```bash
  your_executable -e <original_image.bmp> <secret.txt>
```



#### Decode
```bash
  your_executable -d <stego_image.bmp> [output_file]
```


**Arguments:**
- `-e`: Encoding mode
- `-d`: Decoding mode
- `<original_image.bmp>`: Input bitmap image (must be .bmp)
- `<secret.txt>`: File to hide
- `<stego_image.bmp>`: Image containing hidden data
- `[output_file]`: (optional) Output path for the extracted secret

---

## 📝 File Structure

| File/Folder        | Description                                 |
|--------------------|---------------------------------------------|
| `main.c`           | Main project source code (example)          |
| `README.md`        | This project documentation                  |
| `examples/`        | Example images and scripts                  |
| `tests/`           | Test cases for encoding/decoding            |

---

## 📦 Supported Formats

- **Input Images:** BMP (Bitmap)
- **Secret File:** Any file type (text, image, etc.)

---

## 🛡️ Error Handling

- Only accepts valid BMP images for encoding/decoding.
- Checks capacity before embedding data.
- Validates command-line arguments.
- Outputs clear error messages for invalid inputs or operations.

---

## 👨‍💻 Contribution

Contributions are welcome! Please fork the repo, create a pull request, or open an issue for feedback, suggestions, or improvements.

---

## 📚 License

This project is licensed under the MIT License.

---

## 🙏 Acknowledgments

- Inspired by digital steganography concepts.
- Special thanks to educators and open-source contributors in information security.
