# File-organiser-Application
A lightweight script to automatically organize and rename files in your working directory. It filters files by extension, renames them sequentially, and moves them into a dedicated folder for better structure and cleanliness. 

---

## Features

* Scans the current directory for files.
* Filters files by the specified extension.
* Automatically creates a target folder (e.g., `images/`) if it doesn’t exist.
* Renames files sequentially (`photo-1.jpg`, `photo-2.jpg`, …).
* Moves renamed files into the target folder.

---

## How It Works

The script:

1. Loads all files using `os.listdir()`.
2. Filters files ending with your chosen extension.
3. Creates a folder named `images` if missing.
4. Renames and moves each file inside the folder.
   Logic reference: `arrange_files(files, ".jpg")` in the script. 

---

## Usage

### 1. Place the script in the directory you want to organize.

Your folder should contain the files you want to move.

### 2. Edit the extension (optional)

By default, it processes `.jpg` files.
To modify, update:

```python
arrange_files(files, ".jpg")
```

### 3. Run the script

```bash
python main.py
```

### 4. Check your output

Your organized files will appear inside `/images` renamed as:

```
photo-1.jpg
photo-2.jpg
photo-3.jpg
...
```

---

## Example Directory Before

```
main.py
pic1.jpg
new.jpg
random.png
hello.jpg
```

## After Running

```
main.py
random.png
images/
    photo-1.jpg
    photo-2.jpg
    photo-3.jpg
```

---

## Requirements

* Python 3.x
* No external libraries

---

## Customization

You can modify the target folder name or rename pattern by editing:

```python
os.rename(file, f"images/photo-{i+1}{ext}")
```

