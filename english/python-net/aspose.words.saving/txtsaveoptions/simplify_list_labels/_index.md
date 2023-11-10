---
title: TxtSaveOptions.simplify_list_labels property
linktitle: simplify_list_labels property
articleTitle: simplify_list_labels property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.simplify_list_labels property. Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text."
type: docs
weight: 70
url: /python-net/aspose.words.saving/txtsaveoptions/simplify_list_labels/
---

## TxtSaveOptions.simplify_list_labels property

Specifies whether the program should simplify list labels in case of
complex label formatting not being adequately represented by plain text.

If set to ``True``, numbered list labels are written in simple numeric format
and itemized list labels as simple ASCII characters. The default value is ``False``.




```python
@property
def simplify_list_labels(self) -> bool:
    ...

@simplify_list_labels.setter
def simplify_list_labels(self, value: bool):
    ...

```

### Examples

Shows how to change the appearance of lists when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a bulleted list with five levels of indentation.
builder.list_format.apply_bullet_default()
builder.writeln("Item 1")
builder.list_format.list_indent()
builder.writeln("Item 2")
builder.list_format.list_indent()
builder.writeln("Item 3")
builder.list_format.list_indent()
builder.writeln("Item 4")
builder.list_format.list_indent()
builder.write("Item 5")

# Create a "TxtSaveOptions" object, which we can pass to the document's "save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()

# Set the "simplify_list_labels" property to "True" to convert some list
# symbols into simpler ASCII characters, such as '*', 'o', '+', '>', etc.
# Set the "simplify_list_labels" property to "False" to preserve as many original list symbols as possible.
txt_save_options.simplify_list_labels = simplify_list_labels

doc.save(ARTIFACTS_DIR + "TxtSaveOptions.simplify_list_labels.txt", txt_save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.simplify_list_labels.txt", "rb") as file:
    doc_text = file.read().decode("utf-8-sig")

if simplify_list_labels:
    self.assertEqual(
        "* Item 1\r\n" +
        "  > Item 2\r\n" +
        "    + Item 3\r\n" +
        "      - Item 4\r\n" +
        "        o Item 5\r\n", doc_text)
else:
    self.assertEqual(
        "· Item 1\r\n" +
        "o Item 2\r\n" +
        "§ Item 3\r\n" +
        "· Item 4\r\n" +
        "o Item 5\r\n", doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

