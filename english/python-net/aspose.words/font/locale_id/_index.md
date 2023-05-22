---
title: Font.locale_id property
linktitle: locale_id property
articleTitle: locale_id property
second_title: Aspose.Words for Python
description: "Font.locale_id property. Gets or sets the locale identifier (language) of the formatted characters."
type: docs
weight: 200
url: /python-net/aspose.words/font/locale_id/
---

## Font.locale_id property

Gets or sets the locale identifier (language) of the formatted characters.

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


### Examples

Shows how to set the locale of the text that we are adding with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# If we set the font's locale to English and insert some Russian text,
# the English locale spell checker will not recognize the text and detect it as a spelling error.
builder.font.locale_id = 1033 # en-US
builder.writeln("Привет!")

# Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
builder.font.locale_id = 1049 # ru-RU
builder.writeln("Привет!")

doc.save(ARTIFACTS_DIR + "Font.locale_id.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

