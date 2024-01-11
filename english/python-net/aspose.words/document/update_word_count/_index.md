---
title: Document.update_word_count method
linktitle: update_word_count method
articleTitle: update_word_count method
second_title: Aspose.Words for Python
description: "aspose.words.Document.update_word_count method"
type: docs
weight: 800
url: /python-net/aspose.words/document/update_word_count/
---

## update_word_count() {#default}

Updates word count properties of the document.


```python
def update_word_count(self):
    ...
```

### Remarks

[Document.update_word_count()](./#default) recalculates and updates Characters, Words and Paragraphs
properties in the [Document.built_in_document_properties](../built_in_document_properties/) collection of the [Document](../).

Note that [Document.update_word_count()](./#default) does not update number of lines and pages properties.
Use the [Document.update_word_count()](./#default) overload and pass ``True`` value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included
in the word count.




## update_word_count(update_lines_count) {#bool}

Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.lines](../../../aspose.words.properties/builtindocumentproperties/lines/) property.



```python
def update_word_count(self, update_lines_count: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| update_lines_count | bool | ``True`` if number of lines in the document shall be calculated. |

### Remarks

This method will rebuild page layout of the document.


## Examples

Shows how to update all list labels in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")
builder.write("Ut enim ad minim veniam, " +
              "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.")

# Aspose.Words does not track document metrics like these in real time.
self.assertEqual(0, doc.built_in_document_properties.characters)
self.assertEqual(0, doc.built_in_document_properties.words)
self.assertEqual(1, doc.built_in_document_properties.paragraphs)
self.assertEqual(1, doc.built_in_document_properties.lines)

# To get accurate values for three of these properties, we will need to update them manually.
doc.update_word_count()

self.assertEqual(196, doc.built_in_document_properties.characters)
self.assertEqual(36, doc.built_in_document_properties.words)
self.assertEqual(2, doc.built_in_document_properties.paragraphs)

# For the line count, we will need to call a specific overload of the updating method.
self.assertEqual(1, doc.built_in_document_properties.lines)

doc.update_word_count(True)

self.assertEqual(4, doc.built_in_document_properties.lines)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

