---
title: list_label property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting for this paragraph."
type: docs
weight: 160
url: /python-net/aspose.words/paragraph/list_label/
---

## Paragraph.list_label property

Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting
for this paragraph.



### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")
doc.update_list_labels()

paras = [node.as_paragraph() for node in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)]

# Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
# which start at three and ends at six.
for paragraph in paras:
    if paragraph.list_format.is_list_item:
        print(f"List item paragraph #{paras.index(paragraph)}")

        # This is the text we get when getting when we output this node to text format.
        # This text output will omit list labels. Strip any paragraph formatting characters.
        paragraph_text = paragraph.to_string(aw.SaveFormat.TEXT).strip()
        print(f"\tExported Text: {paragraph_text}")

        label = paragraph.list_label

        # This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
        # this will tell us what position it is on that level.
        print(f"\tNumerical Id: {label.label_value}")

        # Combine them together to include the list label with the text in the output.
        print(f"\tList label combined with text: {label.label_string} {paragraph_text}")
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

