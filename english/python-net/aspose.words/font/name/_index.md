---
title: name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the name of the font."
type: docs
weight: 230
url: /python-net/aspose.words/font/name/
---

## Font.name property

Gets or sets the name of the font.

When getting, returns [Font.name_ascii](../name_ascii/).

When setting, sets [Font.name_ascii](../name_ascii/), [Font.name_bi](../name_bi/), [Font.name_far_east](../name_far_east/)
and [Font.name_other](../name_other/) to the specified value.




### Examples

Shows how to insert formatted text using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Specify font formatting, then add text.
font = builder.font
font.size = 16
font.bold = True
font.color = drawing.Color.blue
font.name = "Courier New"
font.underline = aw.Underline.DASH

builder.write("Hello world!")
```

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc, "Hello world!")

font = run.font
font.name = "Courier New"
font.size = 36
font.highlight_color = drawing.Color.yellow

doc.first_section.body.first_paragraph.append_child(run)
doc.save(ARTIFACTS_DIR + "Font.create_formatted_run.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

