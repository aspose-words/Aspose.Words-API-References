---
title: CustomXmlPropertyCollection class
linktitle: CustomXmlPropertyCollection class
articleTitle: CustomXmlPropertyCollection class
second_title: Aspose.Words for Python
description: "aspose.words.markup.CustomXmlPropertyCollection class. Represents a collection of custom XML attributes or smart tag properties"
type: docs
weight: 60
url: /tr/python-net/aspose.words.markup/customxmlpropertycollection/
---

## CustomXmlPropertyCollection class

Represents a collection of custom XML attributes or smart tag properties.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Remarks

Items are [CustomXmlProperty](../customxmlproperty/) objects.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a property at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(property)](./add/#customxmlproperty) | Adds a property to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ contains(name)](./contains/#str) | Determines whether the collection contains a property with the given name. |
|[ get_by_name(name)](./get_by_name/#str) | Gets a property with the specified name. |
|[ index_of_key(name)](./index_of_key/#str) | Returns the zero-based index of the specified property in the collection. |
|[ remove(name)](./remove/#str) | Removes a property with the specified name from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a property at the specified index. |

### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# Microsoft Word'ün bir belgede metnin bir kısmını bir veri biçimi olarak tanıdığı bir akıllı etiket ortaya çıkar,
# örneğin bir isim, tarih veya adres gibi, ve bunu mor noktalı alt çizgi gösteren bir köprüye dönüştürür.
# Word 2003'te, "Araçlar" -> "Otomatik Düzeltme seçenekleri..." -> "SmartTags" aracılığıyla akıllı etiketleri etkinleştirebiliriz.
# Girdi belgemizde, Microsoft Word'ün akıllı etiket olarak kaydettiği üç nesne bulunmaktadır.
# Akıllı etiketler iç içe olabilir, bu yüzden bu koleksiyon daha fazlasını içerir.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# Bir akıllı etiketin "Properties" üyesi, her akıllı etiket türü için farklı olacak meta verilerini içerir.
# "date" türündeki bir akıllı etiketin özellikleri, yıl, ay ve günü içerir.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# Ayrıca özelliklere, bir anahtar-değer çifti gibi çeşitli yollarla erişebiliriz.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# Aşağıda, özellikler koleksiyonundan öğeleri kaldırmanın üç yolu verilmiştir.
# 1 -  İndeks ile kaldır:
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  İsimle kaldır:
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  Tüm koleksiyonu bir kerede temizle:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../)

