---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

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
* class [OutlineOptions](../)

