---
title: StyleCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "StyleCollection.count property. Gets the number of styles in the collection."
type: docs
weight: 20
url: /ru/python-net/aspose.words/stylecollection/count/
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
# Установите параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles.default_font.name = 'Courier New'
# Если мы добавим стиль типа \"StyleType.Paragraph\", коллекция применит значения
# его свойства \"DefaultParagraphFormat\" к свойству \"ParagraphFormat\" стиля.
styles.default_paragraph_format.first_line_indent = 15
# Добавьте стиль, а затем проверьте, что у него установлены настройки по умолчанию.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

