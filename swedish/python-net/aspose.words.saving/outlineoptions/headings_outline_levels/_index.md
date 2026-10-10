---
title: OutlineOptions.headings_outline_levels property
linktitle: headings_outline_levels property
articleTitle: headings_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.headings_outline_levels property. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline."
type: docs
weight: 70
url: /sv/python-net/aspose.words.saving/outlineoptions/headings_outline_levels/
---

## OutlineOptions.headings_outline_levels property

Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the 
document outline.


```python
@property
def headings_outline_levels(self) -> int:
    ...

@headings_outline_levels.setter
def headings_outline_levels(self, value: int):
    ...

```

### Remarks

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga rubriker på nivåerna 1 till 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Den resulterande PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
# Att klicka på en post i denna disposition tar oss till platsen för dess respektive rubrik.
# Ställ in egenskapen "HeadingsOutlineLevels" till "4" för att utesluta alla rubriker med nivåer över 4 från dispositionen.
options.outline_options.headings_outline_levels = 4
# Om ett dispositionsobjekt har efterföljande objekt på en högre nivå mellan sig själv och nästa objekt på samma eller lägre nivå,
# kommer en pil att visas till vänster om objektet. Detta objekt är "ägaren" till flera sådana "underposter".
# I vårt dokument är dispositionsobjekten från den 5:e rubriknivån underposter till det andra dispositionsobjektet på 4:e nivån,
# den 4:e och 5:e rubriknivåposterna är underposter till den andra 3:e nivåposten, och så vidare.
# I översikten kan vi klicka på pilen för "owner"-posten för att fälla ihop/expandera alla dess underposter.
# Ställ in egenskapen "ExpandedOutlineLevels" till "2" för att automatiskt expandera alla rubriknivå 2 och lägre poster i dispositionen
# och fälla ihop alla nivå 3 och högre poster när vi öppnar dokumentet.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

