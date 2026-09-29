---
title: ListLevel.number_position property
linktitle: number_position property
articleTitle: number_position property
second_title: Aspose.Words for Python
description: "ListLevel.number_position property. Returns or sets the position (in points) of the number or bullet for the list level."
type: docs
weight: 80
url: /tr/python-net/aspose.words.lists/listlevel/number_position/
---

## ListLevel.number_position property

Returns or sets the position (in points) of the number or bullet for the list level.


```python
@property
def number_position(self) -> float:
    ...

@number_position.setter
def number_position(self, value: float):
    ...

```

### Remarks

[ListLevel.number_position](./) corresponds to LeftIndent plus FirstLineIndent of the paragraph.




### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
# Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
# Bir belge oluşturucusunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
# Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelecektir.
# Microsoft Word şablonundan bir liste oluşturun ve onun ilk iki liste seviyesini özelleştirin.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# Bu NumberFormat değeri, yıldız şeklinde madde işareti listesi sembolleri oluşturacaktır.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Paragraflar oluşturun ve özel liste biçimlendirmemizin her iki liste seviyesini onlara uygulayın.
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)
* property [ListLevel.text_position](../text_position/)
* property [ListLevel.tab_position](../tab_position/)

