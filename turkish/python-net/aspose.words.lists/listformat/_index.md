---
title: ListFormat class
linktitle: ListFormat class
articleTitle: ListFormat class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListFormat class. Allows to control what list formatting is applied to a paragraph"
type: docs
weight: 30
url: /tr/python-net/aspose.words.lists/listformat/
---

## ListFormat class

Allows to control what list formatting is applied to a paragraph.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

A paragraph in a Microsoft Word document can be bulleted or numbered.
When a paragraph is bulleted or numbered, it is said that list formatting
is applied to the paragraph.

You do not create objects of the [ListFormat](./) class directly.
You access [ListFormat](./) as a property of another object that can
have list formatting associated with it. At the moment the objects that can
have list formatting are: [Paragraph](../../aspose.words/paragraph/),
[Style](../../aspose.words/style/) and [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies
what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable
to paragraph styles only) allows to specify what list formatting and list level
is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/)
provides access to the list formatting at the current cursor position
inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

The list formatting itself is stored inside a [List](../list/)
object that is stored separately from the paragraphs. The list objects
are stored inside a [ListCollection](../listcollection/) collection. There is a single
[ListCollection](../listcollection/) collection per [Document](../../aspose.words/document/).

The paragraphs do not physically belong to a list. The paragraphs just
reference a particular list object via the [ListFormat.list](./list/) property
and a particular level in the list via the [ListFormat.list_level_number](./list_level_number/) property.
By setting these two properties you control what bullets and numbering is
applied to a paragraph.




### Properties

| Name | Description |
| --- | --- |
| [is_list_item](./is_list_item/) | True when the paragraph has bulleted or numbered formatting applied to it. |
| [list](./list/) | Gets or sets the list this paragraph is a member of. |
| [list_level](./list_level/) | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [list_level_number](./list_level_number/) | Gets or sets the list level number (0 to 8) for the paragraph. |

### Methods

| Name | Description |
| --- | --- |
|[ apply_bullet_default()](./apply_bullet_default/#default) | Starts a new default bulleted list and applies it to the paragraph. |
|[ apply_number_default()](./apply_number_default/#default) | Starts a new default numbered list and applies it to the paragraph. |
|[ list_indent()](./list_indent/#default) | Increases the list level of the current paragraph by one level. |
|[ list_outdent()](./list_outdent/#default) | Decreases the list level of the current paragraph by one level. |
|[ remove_numbers()](./remove_numbers/#default) | Removes numbers or bullets from the current paragraph and sets list level to zero. |

### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
# Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
# Bir belge oluşturucusunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
# Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelecektir.
# Aşağıda, bir belge oluşturucu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
# 1 -  Numaralı bir liste:
# Numaralı listeler, her öğeyi numaralandırarak paragraflarına mantıksal bir sıra verir.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# "ListLevelNumber" özelliğini ayarlayarak, liste seviyesini artırabiliriz
# mevcut liste öğesinde bağımsız bir alt liste başlatmak için.
# "NumberDefault" adlı Microsoft Word liste şablonu, ilk liste seviyesi için liste seviyeleri oluşturmak amacıyla sayılar kullanır.
# Daha derin liste seviyeleri harfler ve küçük harf Roma rakamları kullanır.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Madde işaretli bir liste:
# Bu liste, her paragrafın önüne bir girinti ve madde işareti ("•") ekleyecektir.
# Bu listenin daha derin seviyeleri, "■" ve "○" gibi farklı semboller kullanacaktır.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# "List" bayrağını kaldırarak, sonraki paragrafların liste olarak biçimlendirilmemesi için liste biçimlendirmesini devre dışı bırakabiliriz.
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words.lists](../)

