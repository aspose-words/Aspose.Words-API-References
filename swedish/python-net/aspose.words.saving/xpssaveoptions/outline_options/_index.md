---
title: XpsSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 40
url: /sv/python-net/aspose.words.saving/xpssaveoptions/outline_options/
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
# Infoga rubriker som kan fungera som TOC‑poster på nivå 1, 2 och sedan 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# Skapa ett "XpsSaveOptions"‑objekt som vi kan skicka till dokumentets "Save"‑metod
# för att ändra hur den metoden konverterar dokumentet till .XPS.
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# Det resulterande XPS-dokumentet kommer att innehålla en disposition, en innehållsförteckning som listar rubriker i dokumentkroppen.
# Att klicka på en post i denna disposition tar oss till platsen för dess respektive rubrik.
# Ställ in egenskapen "HeadingsOutlineLevels" till "2" för att utesluta alla rubriker med nivåer över 2 från dispositionen.
# De två sista rubrikerna som vi har infogat ovan kommer inte att visas.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

