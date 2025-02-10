---
title: Font.number_spacing property
linktitle: number_spacing property
articleTitle: number_spacing property
second_title: Aspose.Words for Python
description: "Font.number_spacing property. Gets or sets the spacing type of the numeral being displayed."
type: docs
weight: 290
url: /python-net/aspose.words/font/number_spacing/
---

## Font.number_spacing property

Gets or sets the spacing type of the numeral being displayed.


```python
@property
def number_spacing(self) -> aspose.words.NumSpacing:
    ...

@number_spacing.setter
def number_spacing(self, value: aspose.words.NumSpacing):
    ...

```

### Examples

Shows how to set the spacing type of the numeral.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# This effect is only supported in newer versions of MS Word.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2019)
builder.write('1 ')
builder.write('This is an example')
run = doc.first_section.body.first_paragraph.runs[0]
if run.font.number_spacing == aw.NumSpacing.DEFAULT:
    run.font.number_spacing = aw.NumSpacing.PROPORTIONAL
doc.save(file_name=ARTIFACTS_DIR + 'Fonts.NumberSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

