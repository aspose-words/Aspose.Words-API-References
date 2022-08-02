---
title: clear_formatting method
second_title: Aspose.Words for Python via .NET API Reference
description: "Resets to default font formatting."
type: docs
weight: 550
url: /python-net/aspose.words/font/clear_formatting/
---

## clear_formatting() {#default}

Resets to default font formatting.


```python
def clear_formatting(self):
    ...
```

Removes all font formatting specified explicitly on the object from which
**Font** was obtained so the font formatting will be inherited from
the appropriate parent.




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

* module [aspose.words](../../)
* class [Font](../)

