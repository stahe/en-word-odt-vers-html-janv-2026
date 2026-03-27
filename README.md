# Word/ODT to HTML Website Converter (MkDocs)

🔗 **[View the generated demo site](https://stahe.github.io/en-word-odt-vers-html-janv-2026/)**

---

## 📝 Description

This project aims to provide readers with a Python converter for converting Word or ODT documents into a static HTML website.

When the ODT or DOCX document is suitable, the converter produces a high-quality HTML website using **MkDocs**.

## 🤖 Development background

This converter was initially built by the **Gemini 3** AI. It is the result of successive iterations to finely manage the structure of ODT (OpenDocument Text) documents.
It was subsequently improved by the **ChatGPT 5.2** AI, which produced the converter for Word documents.

## ✨ Features

The `convert.py` script performs the following actions:

* **ODT / DOCX to Markdown conversion**: Analyses the source file to extract its structure.
* **Heading management**: Automatically generates the Table of Contents (TOC) and side navigation.
* **Code Blocks**: Automatic language detection, syntax highlighting and **precise line numbering** (using `start-value` attributes).
* **Lists**: Support for nested and mixed bulleted and numbered lists with correct indentation.
* **Formatting**: Support for *bold*, *italics*, *underline* and *highlighting* (preserving original colours).
* **Images**: Automatic extraction and embedding of images contained in the document.
* **Links**: Hyperlinks or cross-references in the source document are converted into hyperlinks in the HTML document.
* **Footnotes**: Footnotes are supported.
* **Configuration**: Customisation via a `config.py` file (footnotes, Google Analytics, etc.).

## 🚀 Installation

### Prerequisites

* Python 3.x
* The following libraries:

```bash
pip install odfpy unidecode mkdocs mkdocs-material

```

### Project structure

Ensure you have the following files:

* `convert.py`: The conversion script.
* `config.py`: Your configuration file.
* `your-document.odt/docx`: The source document.

## 💻 Usage

1. **Conversion**
Run the script by specifying the source ODT/DOCX file and the configuration file:
```bash
python convert_odt_vxxx.py your-document.odt config.py
python convert_docx_vxx.py your-document.docx config.py
```


*This will generate a `docs/` folder containing the Markdown files and an `mkdocs.yml` file.*
2. **Preview**
To view the site locally:
```bash
python -m mkdocs serve

```


3. **Generation**
To build the static site (`site/` folder):
```bash
python build

```


## ⚙️ Configuration (`config.py`)

The `config.py` file allows you to control the appearance of the site:

* **mkdocs**: General site settings (title, description, Material theme).
* **footer**: Complete HTML code to customise the footer.
* **code**: Language detection rules for syntax highlighting.
* **extra**: Google Analytics (GA4) configuration.

## 📄 Licence

This tutorial course written by **Serge Tahé** is made available to the public under the terms of the:
*Creative Commons Attribution – Non-Commercial – ShareAlike 3.0 Unported Licence.*
