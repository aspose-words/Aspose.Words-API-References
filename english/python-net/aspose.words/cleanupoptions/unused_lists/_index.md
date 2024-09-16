---
title: CleanupOptions.unused_lists property
linktitle: unused_lists property
articleTitle: unused_lists property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_lists property. Specifies whether unused list and list definitions should be removed from document"
type: docs
weight: 40
url: /python-net/aspose.words/cleanupoptions/unused_lists/
---

## CleanupOptions.unused_lists property

Specifies whether unused list and list definitions should be removed from document.
Default value is ``True``.



```python
@property
def unused_lists(self) -> bool:
    ...

@unused_lists.setter
def unused_lists(self, value: bool):
    ...

```

### Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# Combined with the built-in styles, the document now has eight styles.
# A custom style is marked as "used" while there is any text within the document
# formatted in that style. This means that the 4 styles we added are currently unused.
self.assertEqual(8, doc.styles.count)
# Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Now, there is one unused character style and one unused list style.
# The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Removing every node that a custom style is applied to marks it as "unused" again.
# Rerun the Cleanup method to remove them.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

