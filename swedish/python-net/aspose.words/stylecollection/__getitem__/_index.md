---
title: StyleCollection indexer
linktitle: StyleCollection indexer
articleTitle: StyleCollection indexer
second_title: Aspose.Words for Python
description: "StyleCollection indexer. Gets a style by index."
type: docs
weight: 10
url: /sv/python-net/aspose.words/stylecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a style by index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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

