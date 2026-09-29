---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /sv/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
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
# Infoga rubriker som kan fungera som innehållsförteckningsposter på nivå 1 och 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
save_options = aw.saving.PdfSaveOptions()
# Den resulterande PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
# Att klicka på en post i denna disposition tar oss till platsen för dess respektive rubrik.
# Ställ in egenskapen "HeadingsOutlineLevels" till "5" för att inkludera alla rubriker på nivå 5 och lägre i dispositionen.
save_options.outline_options.headings_outline_levels = 5
# Detta dokument innehåller rubriker på nivå 1 och 5, och inga rubriker på nivå 2, 3 och 4.
# Den resulterande PDF‑dokumentet kommer att behandla dispositionsnivåerna 2, 3 och 4 som "saknade".
# Ställ in egenskapen "CreateMissingOutlineLevels" till "true" för att inkludera alla saknade nivåer i dispositionen,
# och lämna tomma dispositionsposter eftersom det inte finns några användbara rubriker.
# Ställ in egenskapen "CreateMissingOutlineLevels" till "false" för att ignorera saknade dispositionsnivåer,
# och behandla rubriker på dispositionsnivå 5 som nivå 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

