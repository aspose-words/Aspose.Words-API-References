---
title: XpsSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 40
url: /de/python-net/aspose.words.saving/xpssaveoptions/outline_options/
---

## XpsSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Note that [OutlineOptions.expanded_outline_levels](../../outlineoptions/expanded_outline_levels/) option will not work when saving to XPS.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

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
# Erstellen Sie ein "XpsSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# Das ausgegebene XPS‑Dokument enthält ein Inhaltsverzeichnis, das Überschriften im Dokumentkörper auflistet.
# Ein Klick auf einen Eintrag in diesem Inhaltsverzeichnis führt uns zur Position der jeweiligen Überschrift.
# Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "2", um alle Überschriften mit einem Niveau über 2 vom Inhaltsverzeichnis auszuschließen.
# Die beiden zuletzt eingefügten Überschriften oben werden nicht angezeigt.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

