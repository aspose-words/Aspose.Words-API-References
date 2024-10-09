---
title: NumeralFormat enumeration
linktitle: NumeralFormat enumeration
articleTitle: NumeralFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.NumeralFormat enumeration. Indicates the symbol set that is used to represent numbers while rendering to fixed page formats."
type: docs
weight: 480
url: /python-net/aspose.words.saving/numeralformat/
---

## NumeralFormat enumeration

Indicates the symbol set that is used to represent numbers
while rendering to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| EUROPEAN | European numerals: 0123456789. |
| ARABIC_INDIC | Numerals used in Arabic: ٠١٢٣٤٥٦٧٨٩. Unicode range U+0660 - u+0669. |
| EASTERN_ARABIC_INDIC | Numerals used in Persian and Urdu: ۰۱۲۳۴۵۶۷۸۹. Unicode range U+06F0 - u+06F9. |
| CONTEXT | Symbol set is decided from context(locale and RTL property). |
| SYSTEM | THIS OPTION IS NOT SUPPORTED. Symbol set is decided from regional settings. |

### Examples

Shows how to set the numeral format used when saving to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.locale_id = 4096  # CultureInfo("ar-AR").lcid
builder.writeln('1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100')
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
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.set_numeral_format.pdf', options)
```

### See Also

* module [aspose.words.saving](../)

