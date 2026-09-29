---
title: StyleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "StyleCollection.add method. Creates a new user defined style and adds it the collection."
type: docs
weight: 60
url: /tr/python-net/aspose.words/stylecollection/add/
---

## add(type, name) {#styletype_str}

Creates a new user defined style and adds it the collection.


```python
def add(self, type: aspose.words.StyleType, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [StyleType](../../styletype/) | A [StyleType](../../styletype/) value that specifies the type of the style to create. |
| name | str | Case sensitive name of the style to create. |

### Remarks

You can create character, paragraph or a list style.

When creating a list style, the style is created with default numbered list formatting (1 \\ a \\ i).

Throws an exception if a style with this name already exists.




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

