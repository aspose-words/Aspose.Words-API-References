---
title: List.is_list_style_reference property
linktitle: is_list_style_reference property
articleTitle: is_list_style_reference property
second_title: Aspose.Words for Python
description: "List.is_list_style_reference property. Returns ``True`` if this list is a reference to a list style."
type: docs
weight: 30
url: /tr/python-net/aspose.words.lists/list/is_list_style_reference/
---

## List.is_list_style_reference property

Returns ``True`` if this list is a reference to a list style.



```python
@property
def is_list_style_reference(self) -> bool:
    ...

```

### Remarks

Note, modifying properties of a list that is a reference to list style has no effect.
The list formatting specified in the list style itself always takes precedence.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
# Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
# Bir belge oluşturucusunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
# Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelecektir.
# Bir stil içinde tüm bir List nesnesi içerebiliriz.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Listemizdeki tüm liste seviyelerinin görünümünü değiştirin.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Bir stil içindeki listeden başka bir liste oluşturun.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Listemizin biçimlendireceği bazı liste öğeleri ekleyin.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Liste stiline dayalı başka bir liste oluşturun ve uygulayın.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)
* property [List.style](../style/)
* property [List.is_list_style_definition](../is_list_style_definition/)

