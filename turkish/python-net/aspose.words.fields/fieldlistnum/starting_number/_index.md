---
title: FieldListNum.starting_number property
linktitle: starting_number property
articleTitle: starting_number property
second_title: Aspose.Words for Python
description: "FieldListNum.starting_number property. Gets or sets the starting value for this field."
type: docs
weight: 50
url: /tr/python-net/aspose.words.fields/fieldlistnum/starting_number/
---

## FieldListNum.starting_number property

Gets or sets the starting value for this field.


```python
@property
def starting_number(self) -> str:
    ...

@starting_number.setter
def starting_number(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# LISTNUM alanları, her LISTNUM alanında artan bir sayı gösterir.
# Bu alanların ayrıca numaralı listeleri taklit etmemizi sağlayan çeşitli seçenekleri vardır.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
# Bu alan "0)" gösterecek.
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# LISTNUM alanları her liste seviyesinin ayrı sayımlarını tutar.
# Aynı paragrafta başka bir LISTNUM alanı ile bir LISTNUM alanı eklemek
# sayımı artırmak yerine liste seviyesini artırır.
# Sonraki alan, yukarıda başlattığımız sayımı devam ettirecek ve 1. liste seviyesinde "1" değerini gösterecek.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Bu alan 2. liste seviyesinde bir sayım başlatacak. "1" değerini gösterecek.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Bu alan 3. liste seviyesinde bir sayım başlatacak. "1" değerini gösterecek.
# Farklı liste seviyeleri farklı biçimlendirmelere sahiptir,
# bu nedenle bu alanlar birleştirildiğinde "1)a)i)" değerini gösterir.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Eklediğimiz bir sonraki LISTNUM alanı, liste seviyesinde sayımı devam ettirecek
# önceki LISTNUM alanının bulunduğu seviyede.
# "ListLevel" özelliğini kullanarak farklı bir liste seviyesine atlayabiliriz.
# Bu LISTNUM alanı liste seviyesi 3'te kalırsa, "ii)" gösterirdi,
# ancak, onu liste seviyesi 2'ye taşıdığımız için, sayımı o seviyede sürdürür ve "b)" gösterir.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Alanı farklı bir AUTONUM alan türünü taklit ettirmek için ListName özelliğini ayarlayabiliriz.
# "NumberDefault" AUTONUM'u taklit eder, "OutlineDefault" AUTONUMOUT'u taklit eder,
# ve "LegalDefault" AUTONUMLGL alanlarını taklit eder.
# "OutlineDefault" liste adı, başlangıç numarası 1 olduğunda "I." gösterir.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# ListName önceki alandan devralınmaz, bu yüzden her yeni alan için ayarlamamız gerekir.
# Bu alan, farklı liste adıyla sayımı sürdürür ve "II." gösterir.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

