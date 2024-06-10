---
title: Style.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "Style.equals method. Compares with the specified style"
type: docs
weight: 230
url: /python-net/aspose.words/style/equals/
---

## equals(style) {#style}

Compares with the specified style.
Styles Istds are compared for built-in styles only.
Styles defaults are not included in comparison.
Base style, linked style and next paragraph style are recursively compared.


```python
def equals(self, style: aspose.words.Style):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | [Style](../) |  |

### Examples

Shows how to use style aliases.

```python
doc = aw.Document(file_name=MY_DIR + 'Style with alias.docx')
# This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
# If a style's name has multiple values separated by commas, each clause is a separate alias.
style = doc.styles.get_by_name('MyStyle')
self.assertSequenceEqual(['MyStyle Alias 1', 'MyStyle Alias 2'], style.aliases)
self.assertEqual('Title', style.base_style_name)
self.assertEqual('MyStyle Char', style.linked_style_name)
# We can reference a style using its alias, as well as its name.
self.assertEqual(doc.styles.get_by_name('MyStyle Alias 1'), doc.styles.get_by_name('MyStyle Alias 2'))
builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle Alias 1')
builder.writeln('Hello world!')
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle Alias 2')
builder.write('Hello again!')
self.assertEqual(doc.first_section.body.paragraphs[0].paragraph_format.style, doc.first_section.body.paragraphs[1].paragraph_format.style)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

