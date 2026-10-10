---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /tr/python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


```python
@property
def built_in(self) -> bool:
    ...

```

### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()
# Microsoft Word kullanarak veya programlı olarak Aspose.Words ile bir belge oluşturduğumuzda,
# belge, görünümünü değiştirmek için metnine uygulanacak bir stil koleksiyonu ile gelecektir.
# Bu yerleşik stillere belgenin "Styles" koleksiyonu aracılığıyla erişebiliriz.
# Bu stillerin tümü "BuiltIn" bayrağının "true" olarak ayarlanmış olacaktır.
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Özel bir stil oluşturun ve koleksiyona ekleyin.
# Böyle özel stillerin "BuiltIn" bayrağı "false" olarak ayarlanacaktır.
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

