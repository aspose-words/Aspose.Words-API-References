---
title: update_list_labels method
second_title: Aspose.Words for Python via .NET API Reference
description: "Updates list labels for all list items in the document."
type: docs
weight: 730
url: /python-net/aspose.words/document/update_list_labels/
---

## update_list_labels() {#default}

Updates list labels for all list items in the document.


```python
def update_list_labels(self):
    ...
```

This method updates list label properties such as [ListLabel.label_value](../../../aspose.words.lists/listlabel/label_value/) and
[ListLabel.label_string](../../../aspose.words.lists/listlabel/label_string/) for each [Paragraph.list_label](../../paragraph/list_label/) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required
because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.




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
* class [Document](../)

