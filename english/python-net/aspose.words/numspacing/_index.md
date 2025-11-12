---
title: NumSpacing enumeration
linktitle: NumSpacing enumeration
articleTitle: NumSpacing enumeration
second_title: Aspose.Words for Python
description: "aspose.words.NumSpacing enumeration. Specifies possible values in which numeral spacing can be displayed."
type: docs
weight: 840
url: /python-net/aspose.words/numspacing/
---

## NumSpacing enumeration

Specifies possible values in which numeral spacing can be displayed.


### Members

| Name | Description |
| --- | --- |
| DEFAULT | Specifies that numerals are displayed in the font’s default form. |
| PROPORTIONAL | Specifies that the forms of the numerals designed as proportionally spaced are displayed if supported by the font. |
| TABULAR | Specifies that the forms of the numerals designed as tabular are displayed if supported by the font. |

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

* module [aspose.words](../)

