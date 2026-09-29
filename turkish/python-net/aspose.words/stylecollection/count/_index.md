---
title: StyleCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "StyleCollection.count property. Gets the number of styles in the collection."
type: docs
weight: 20
url: /tr/python-net/aspose.words/stylecollection/count/
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
# Bu koleksiyona daha sonra ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.default_font.name = 'Courier New'
# \"StyleType.Paragraph\" stilini eklersek, koleksiyon değerlerini uygulayacaktır
# bu stilin \"DefaultParagraphFormat\" özelliğini stilin \"ParagraphFormat\" özelliğine uygulayacaktır.
styles.default_paragraph_format.first_line_indent = 15
# Bir stil ekleyin ve ardından varsayılan ayarlara sahip olduğunu doğrulayın.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

