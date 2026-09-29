---
title: ListFormat.list_level property
linktitle: list_level property
articleTitle: list_level property
second_title: Aspose.Words for Python
description: "ListFormat.list_level property. Returns the list level formatting plus any formatting overrides applied to the current paragraph."
type: docs
weight: 30
url: /tr/python-net/aspose.words.lists/listformat/list_level/
---

## ListFormat.list_level property

Returns the list level formatting plus any formatting overrides applied to the current paragraph.


```python
@property
def list_level(self) -> aspose.words.lists.ListLevel:
    ...

```

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
* class [ListFormat](../)

