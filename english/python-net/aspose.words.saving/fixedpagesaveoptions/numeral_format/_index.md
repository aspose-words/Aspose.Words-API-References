---
title: FixedPageSaveOptions.numeral_format property
linktitle: numeral_format property
articleTitle: numeral_format property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.numeral_format property. Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals"
type: docs
weight: 40
url: /python-net/aspose.words.saving/fixedpagesaveoptions/numeral_format/
---

## FixedPageSaveOptions.numeral_format property

Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals.
European numerals are used by default.



```python
@property
def numeral_format(self) -> aspose.words.saving.NumeralFormat:
    ...

@numeral_format.setter
def numeral_format(self, value: aspose.words.saving.NumeralFormat):
    ...

```

### Remarks

If the value of this property is changed and page layout is already built then
[Document.update_page_layout()](../../../aspose.words/document/update_page_layout/#default) is invoked automatically to update any changes.



### Examples

Shows how to set the numeral format used when saving to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.locale_id = 4096 # CultureInfo("ar-AR").lcid
builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "numeral_format" property to "NumeralFormat.ARABIC_INDIC" to
# use glyphs from the U+0660 to U+0669 range as numbers.
# Set the "numeral_format" property to "NumeralFormat.CONTEXT" to
# look up the locale to determine what number of glyphs to use.
# Set the "numeral_format" property to "NumeralFormat.EASTERN_ARABIC_INDIC" to
# use glyphs from the U+06F0 to U+06F9 range as numbers.
# Set the "numeral_format" property to "NumeralFormat.EUROPEAN" to use european numerals.
# Set the "numeral_format" property to "NumeralFormat.SYSTEM" to determine the symbol set from regional settings.
options.numeral_format = numeral_format

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.set_numeral_format.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

