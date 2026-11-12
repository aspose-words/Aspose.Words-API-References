---
title: ListFormat.list_indent method
linktitle: list_indent method
articleTitle: list_indent method
second_title: Aspose.Words for Python
description: "ListFormat.list_indent method. Increases the list level of the current paragraph by one level."
type: docs
weight: 70
url: /tr/python-net/aspose.words.lists/listformat/list_indent/
---

## list_indent() {#default}

Increases the list level of the current paragraph by one level.


```python
def list_indent(self):
    ...
```

### Remarks

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting
for each level specifies what bullet or number is used, left indent, space between
the bullet and text etc.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
# Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
# Bir belge oluşturucusunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
# Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelecektir.
# Aşağıda bir belge oluşturucu ile oluşturabileceğimiz iki tür liste bulunmaktadır.
# 1 -  Madde işaretli bir liste:
# Bu liste, her paragrafın önüne bir girinti ve madde işareti ("•") ekleyecektir.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Madde işaretli listeyi sonlandırın.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  Numaralı bir liste:
# Numaralı listeler, her öğeyi numaralandırarak paragraflarına mantıksal bir sıra verir.
builder.list_format.apply_number_default()
# Bu paragraf ilk öğedir. Numaralı bir listenin ilk öğesi "1." list öğesi simgesi olarak sahip olacaktır.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# "ListIndent" metodunu çağırarak geçerli liste seviyesini artırın,
# bu, ilk liste seviyesinin geçerli öğesinde daha derin bir girinti ile yeni, bağımsız bir liste başlatacaktır.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Bunlar, ikinci liste seviyesinin ilk üç liste öğesidir ve bir sayımı koruyacaktır
# ilk liste seviyesinin sayımından bağımsızdır. Geçerli liste formatına göre,
# "a.", "b." ve "c." sembollerine sahip olacaklardır.
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# "ListOutdent" metodunu çağırarak önceki liste seviyesine dönün.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Bu iki paragraf ilk liste seviyesinin sayımını sürdürecektir.
# Bu öğeler "2." ve "3." sembollerine sahip olacaktır
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Eğer liste seviyesini daha önce öğeler eklediğimiz bir seviyeye yükseltirsek,
# iç içe liste önceki listeden ayrı olacak ve numaralandırması baştan başlayacaktır.
# Bu liste öğeleri "a.", "b.", "c.", "d.", ve "e" sembollerine sahip olacak.
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Liste seviyesini tekrar dışa kaydır.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Numaralı listeyi sonlandır.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

