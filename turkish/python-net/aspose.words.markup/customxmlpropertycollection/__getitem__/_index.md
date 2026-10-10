---
title: CustomXmlPropertyCollection indexer
linktitle: CustomXmlPropertyCollection indexer
articleTitle: CustomXmlPropertyCollection indexer
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection indexer. Gets a property at the specified index."
type: docs
weight: 10
url: /tr/python-net/aspose.words.markup/customxmlpropertycollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a property at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)

