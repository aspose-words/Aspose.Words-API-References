---
title: SectionLayoutMode enumeration
linktitle: SectionLayoutMode enumeration
articleTitle: SectionLayoutMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.SectionLayoutMode enumeration. Specifies the layout mode for a section allowing to define the document grid behavior."
type: docs
weight: 1160
url: /de/python-net/aspose.words/sectionlayoutmode/
---

## SectionLayoutMode enumeration

Specifies the layout mode for a section allowing to define the document grid behavior.


### Members

| Name | Description |
| --- | --- |
| DEFAULT | Specifies that no document grid shall be applied to the contents of the corresponding section in the document. |
| GRID | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will not be automatically aligned with gridlines on typing. |
| LINE_GRID | Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page. |
| SNAP_TO_CHARS | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line.  Characters will be automatically aligned with gridlines on typing. |

### Examples

Shows how to specify a for the number of characters that each line may have.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aktivieren Sie das Pitching und verwenden Sie es anschließend, um die Anzahl der Zeichen pro Zeile in diesem Abschnitt festzulegen.
builder.page_setup.layout_mode = aw.SectionLayoutMode.GRID
builder.page_setup.characters_per_line = 10
# Die Anzahl der Zeichen hängt ebenfalls von der Schriftgröße ab.
doc.styles.get_by_name('Normal').font.size = 20
self.assertEqual(8, doc.first_section.page_setup.characters_per_line)
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.CharactersPerLine.docx')
```

Shows how to specify a limit for the number of lines that each page may have.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aktivieren Sie das Pitching und verwenden Sie es anschließend, um die Anzahl der Zeilen pro Seite in diesem Abschnitt festzulegen.
# Eine ausreichend große Schriftgröße schiebt einige Zeilen auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder.page_setup.layout_mode = aw.SectionLayoutMode.LINE_GRID
builder.page_setup.lines_per_page = 15
builder.paragraph_format.snap_to_grid = True
i = 0
while i < 30:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LinesPerPage.docx')
```

### See Also

* module [aspose.words](../)

