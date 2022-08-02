---
title: Underline enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Indicates type of the underline applied to a font."
type: docs
weight: 1250
url: /python-net/aspose.words/underline/
---

## Underline enumeration

Indicates type of the underline applied to a font.


### Members

| Name | Description |
| --- | --- |
| NONE |  |
| SINGLE |  |
| WORDS |  |
| DOUBLE |  |
| DOTTED |  |
| THICK |  |
| DASH |  |
| DASH_LONG |  |
| DOT_DASH |  |
| DOT_DOT_DASH |  |
| WAVY |  |
| DOTTED_HEAVY |  |
| DASH_HEAVY |  |
| DASH_LONG_HEAVY |  |
| DOT_DASH_HEAVY |  |
| DOT_DOT_DASH_HEAVY |  |
| WAVY_HEAVY |  |
| WAVY_DOUBLE |  |

### Examples

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("For more information, please visit the ")

# Insert a hyperlink and emphasize it with custom formatting.
# The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = drawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink("Google website", "https://www.google.com", False)
builder.font.clear_formatting()
builder.writeln(".")

# Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_hyperlink.docx")
```

### See Also

* module [aspose.words](../)

