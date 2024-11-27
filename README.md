
# **Convert to WebP Quick Action for macOS**

This repository provides an Automator workflow that allows macOS users to easily convert image files (JPG/PNG) to WebP format. The workflow is accessible directly from the Finder's **Quick Actions** menu and adapts to your macOS environment, using either the built-in `sips` tool or Google's `cwebp` utility.

## **Features**
- Converts image files (JPG, PNG, etc.) to WebP format.
- Detects whether your macOS version supports WebP conversion via `sips`.
- Falls back to `cwebp` for robust compatibility.
- Accessible via right-click in Finder for quick and seamless operation.

---

## **Installation**

1. **Download the Workflow File:**
   - Clone or download this repository.
   - Locate the `.workflow` file (e.g., `Convert to WebP.workflow`).

2. **Install the Workflow:**
   - Double-click the `.workflow` file.
   - It will open in **Automator**. Click **Install** to add it to your macOS **Quick Actions**.

---

## **Using the Workflow**

1. **Access the Quick Action:**
   - Open Finder and right-click on an image file (e.g., JPG or PNG).
   - Select `Quick Actions > Convert to WebP`.

2. **Output:**
   - The WebP file will be saved in the same directory as the original image, with the `.webp` extension.

---

## **System Requirements**

### **Option 1: Using `sips`**
- macOS **Ventura (13.0)** or later supports WebP conversion natively with the `sips` tool.
- To check your macOS version:
  ```bash
  sw_vers
  ```

### **Option 2: Using `cwebp`**
If you are running an older macOS version or `sips` does not support WebP, you need to install Google's `cwebp` tool.

#### **Install cwebp via Homebrew:**
1. Install [Homebrew](https://brew.sh/) (if not already installed):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Install the WebP tools:
   ```bash
   brew install webp
   ```

---

## **How It Works**

1. The workflow checks if the built-in `sips` tool can handle WebP conversion.
2. If supported, it uses `sips` to convert the image.
3. If not supported, it falls back to `cwebp` (if installed).
4. If neither `sips` nor `cwebp` is available, the workflow will display an error.

---

## **Troubleshooting**

1. **Ensure macOS is up-to-date:**
   - If `sips` does not support WebP, ensure your macOS version is Ventura (13.0) or later.
   - Update macOS via `System Preferences > Software Update`.

2. **Install cwebp:**
   - Follow the instructions under **Option 2: Using `cwebp`** above.

3. **Error: "Neither sips nor cwebp is available":**
   - Make sure `cwebp` is installed and accessible by running:
     ```bash
     command -v cwebp
     ```

4. **Reinstall Workflow:**
   - If the Quick Action doesn't appear, reinstall the workflow and ensure it is set to handle image files.

---

## **Customizing the Workflow**
To modify the behavior or add additional features:
1. Open **Automator**.
2. Locate and open the `Convert to WebP.workflow` file.
3. Adjust the script or settings as needed.

---

## **License**
This project is licensed under the MIT License. See the LICENSE file for details.
