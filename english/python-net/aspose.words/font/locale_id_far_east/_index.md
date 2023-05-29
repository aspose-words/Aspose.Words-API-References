---
title: Font.locale_id_far_east property
linktitle: locale_id_far_east property
articleTitle: locale_id_far_east property
second_title: Aspose.Words for Python
description: "Font.locale_id_far_east property. Gets or sets the locale identifier (language) of the formatted Asian characters."
type: docs
weight: 220
url: /python-net/aspose.words/font/locale_id_far_east/
---

## Font.locale_id_far_east property

Gets or sets the locale identifier (language) of the formatted Asian characters.

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


### Examples

Shows how to insert and format text in a Far East language.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Specify font settings that the document builder will apply to any text that it inserts.
builder.font.name = "Courier New"
builder.font.locale_id = 1033 # en-US

# Name "FarEast" equivalents for our font and locale.
# If the builder inserts Asian characters with this Font configuration, then each run that contains
# these characters will display them using the "FarEast" font/locale instead of the default.
# This could be useful when a western font does not have ideal representations for Asian characters.
builder.font.name_far_east = "SimSun"
builder.font.locale_id_far_east = 2052 # zh-CN

# This text will be displayed in the default font/locale.
builder.writeln("Hello world!")

# Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
builder.writeln("你好世界")

doc.save(ARTIFACTS_DIR + "Font.far_east.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

