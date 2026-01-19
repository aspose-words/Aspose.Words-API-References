---
title: WarningSource enumeration
linktitle: WarningSource enumeration
articleTitle: WarningSource enumeration
second_title: Aspose.Words for Python
description: "aspose.words.WarningSource enumeration. Specifies the module that produces a warning during document loading or saving."
type: docs
weight: 1440
url: /python-net/aspose.words/warningsource/
---

## WarningSource enumeration

Specifies the module that produces a warning during document loading or saving.


### Members

| Name | Description |
| --- | --- |
| UNKNOWN | The warning source is not specified. |
| LAYOUT | Module that builds a document layout. |
| DRAWING_ML | Module that renders DrawingML shapes. |
| OFFICE_MATH | Module that renders OfficeMath. |
| SHAPES | Module that renders ordinary shapes. |
| METAFILE | Module that renders metafiles. |
| XPS | Module that renders XPS. |
| PDF | Module that renders PDF. |
| IMAGE | Module that renders images. |
| DOCX | Module that reads/writes DOCX files. |
| DOC | Module that reads/writes binary DOC files. |
| TEXT | Module that reads/writes plaintext files. |
| RTF | Module that reads/writes RTF files. |
| WORD_ML | Module that reads/writes WML files. |
| NRX | Common modules that are shared between DOCX/WML reader/writer modules. |
| ODT | Module that reads/writes ODT files. |
| HTML | Module that reads/writes HTML/MHTML files. |
| VALIDATOR | Module that verifies model consistency and validity. |
| XAML | Module that reads/writes Xaml files. |
| SVM | Module that reads Svm files. |
| MATH_ML | Module that reads W3C MathML files. |
| FONT | Module that reads font files. |
| SVG | Module that reads SVG files. |
| MARKDOWN | Module that reads/writes Markdown files. |
| CHM | Module that reads CHM files. |
| EPUB | Module that reads/writes EPUB files. |
| XML | Module that reads XML files. |
| XLSX | Module that writes XLSX files. |
| DOCLING | Module that writes Docling JSON files. |

### Examples

Shows how to work with the warning source.

```python
doc = aw.Document(file_name=MY_DIR + 'Emphases markdown warning.docx')
warnings = aw.WarningInfoCollection()
doc.warning_callback = warnings
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.EmphasesWarningSourceMarkdown.md')
for warning_info in warnings:
    if warning_info.source == aw.WarningSource.MARKDOWN:
        self.assertEqual('The (*, 0:11) cannot be properly written into Markdown.', warning_info.description)
```

### See Also

* module [aspose.words](../)

