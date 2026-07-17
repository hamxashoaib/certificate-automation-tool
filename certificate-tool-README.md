# Certificate Automation Tool

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Pillow](https://img.shields.io/badge/Pillow-Image%20Processing-green)

A Python script that auto-generates personalized certificates from a template image and a list of names, replacing what used to be manual, one-by-one design work for each event. Originally built for HackerRank IUB Chapter events.

## How It Works

1. Reads a list of names from a CSV file
2. Takes a certificate template image (with a blank space for the name)
3. Overlays each name onto a copy of the template, automatically centered
4. Saves each certificate as a separate image file, named after the recipient

## Tech Stack

- **Python**
- **Pillow (PIL)** image processing and text rendering

## Setup

1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
2. Add your certificate template image as `template.png` in the project folder
3. Add a `.ttf` font file as `font.ttf` (any font you want the names displayed in)
4. Fill in `names.csv` with the list of recipient names (one column, header: `name`)
5. Adjust `TEXT_POSITION_Y`, `FONT_SIZE`, and `TEXT_COLOR` in the script to match where the name should appear on your specific template
6. Run:
   ```
   python certificate_generator.py
   ```
7. Generated certificates will appear in the `certificates/` folder, one file per name

## Example

Input (`names.csv`):
```
name
Ali Raza
Ayesha Khan
```

Output:
```
certificates/Ali_Raza.png
certificates/Ayesha_Khan.png
```

## Notes

- The script automatically centers each name horizontally based on its text width, so it works with names of different lengths without manual adjustment
- Vertical position is fixed (set once per template) since certificate templates typically have a consistent layout

## About Me

I'm **Hamza Shoaib**, a BS Artificial Intelligence student at The Islamia University of Bahawalpur, focused on AI agents, automation, and applied GenAI. I built this tool to automate certificate generation for HackerRank IUB Chapter events.

- LinkedIn: [linkedin.com/in/ch-hamza-shoaib](https://linkedin.com/in/ch-hamza-shoaib)
- GitHub: [github.com/hamxashoaib](https://github.com/hamxashoaib)

## Screenshots

*(Add a sample generated certificate here)*
