---
title: StyleCollection indexer
linktitle: StyleCollection indexer
articleTitle: StyleCollection indexer
second_title: Aspose.Words for Python
description: "StyleCollection indexer. Gets a style by index."
type: docs
weight: 10
url: /ar/python-net/aspose.words/stylecollection/__getitem__/
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
# تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.default_font.name = 'Courier New'
# إذا أضفنا نمطًا من نوع \"StyleType.Paragraph\"، ستطبق المجموعة قيم
# خاصية \"DefaultParagraphFormat\" إلى خاصية \"ParagraphFormat\" للنمط.
styles.default_paragraph_format.first_line_indent = 15
# أضف نمطًا، ثم تحقق من أنه يحتوي على الإعدادات الافتراضية.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

