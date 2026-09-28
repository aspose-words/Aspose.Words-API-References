---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 260
url: /de/python-net/aspose.words.saving/pdfsaveoptions/outline_options/
---

## PdfSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outline_options](./) class.




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

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie Überschriften ein, die als TOC‑Einträge der Ebenen 1 und 5 dienen können.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.PdfSaveOptions()
# Das ausgegebene PDF-Dokument enthält ein Inhaltsverzeichnis, das eine Gliederung ist und die Überschriften im Dokumentkörper auflistet.
# Ein Klick auf einen Eintrag in diesem Inhaltsverzeichnis führt uns zur Position der jeweiligen Überschrift.
# Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "5", um alle Überschriften der Ebenen 5 und darunter im Inhaltsverzeichnis aufzunehmen.
save_options.outline_options.headings_outline_levels = 5
# Dieses Dokument enthält Überschriften der Ebenen 1 und 5 und keine Überschriften der Ebenen 2, 3 und 4.
# Das ausgegebene PDF-Dokument behandelt die Inhaltsverzeichnisebenen 2, 3 und 4 als "missing".
# Setzen Sie die Eigenschaft "CreateMissingOutlineLevels" auf "true", um alle fehlenden Ebenen im Inhaltsverzeichnis aufzunehmen,
# wodurch leere Inhaltsverzeichniseinträge entstehen, da keine nutzbaren Überschriften vorhanden sind.
# Setzen Sie die Eigenschaft "CreateMissingOutlineLevels" auf "false", um fehlende Inhaltsverzeichnisebenen zu ignorieren,
# und behandeln Sie die Überschriften der Ebene 5 im Inhaltsverzeichnis als Ebene 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

