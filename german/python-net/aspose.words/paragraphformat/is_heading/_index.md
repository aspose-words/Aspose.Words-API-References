---
title: ParagraphFormat.is_heading property
linktitle: is_heading property
articleTitle: is_heading property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_heading property. True when the paragraph style is one of the built-in Heading styles."
type: docs
weight: 140
url: /de/python-net/aspose.words/paragraphformat/is_heading/
---

## ParagraphFormat.is_heading property

True when the paragraph style is one of the built-in Heading styles.


```python
@property
def is_heading(self) -> bool:
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie Überschriften ein, die als TOC‑Einträge der Ebenen 1, 2 und anschließend 3 dienen können.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# Das ausgegebene PDF-Dokument enthält ein Inhaltsverzeichnis, das eine Gliederung ist und die Überschriften im Dokumentkörper auflistet.
# Ein Klick auf einen Eintrag in diesem Inhaltsverzeichnis führt uns zur Position der jeweiligen Überschrift.
# Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "2", um alle Überschriften mit einem Niveau über 2 vom Inhaltsverzeichnis auszuschließen.
# Die beiden zuletzt eingefügten Überschriften oben werden nicht angezeigt.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

