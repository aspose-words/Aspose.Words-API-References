---
title: StyleCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "StyleCollection.count property. Gets the number of styles in the collection."
type: docs
weight: 20
url: /sv/python-net/aspose.words/stylecollection/count/
---

## StyleCollection.count property

Gets the number of styles in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add a Style to a document's styles collection.

```python
doc = aw.Document()
styles = doc.styles
# Ställ in standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.default_font.name = 'Courier New'
# Om vi lägger till en stil av typen \"StyleType.Paragraph\" kommer samlingen att tillämpa värdena för
# dess egenskap \"DefaultParagraphFormat\" på stilens egenskap \"ParagraphFormat\".
styles.default_paragraph_format.first_line_indent = 15
# Lägg till en stil och verifiera sedan att den har standardinställningarna.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

