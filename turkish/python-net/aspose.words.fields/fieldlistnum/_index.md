---
title: FieldListNum class
linktitle: FieldListNum class
articleTitle: FieldListNum class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldListNum class. Implements the LISTNUM field"
type: docs
weight: 660
url: /tr/python-net/aspose.words.fields/fieldlistnum/
---

## FieldListNum class

Implements the LISTNUM field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




**Inheritance:** [FieldListNum](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldListNum()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [has_list_name](./has_list_name/) | Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [list_level](./list_level/) | Gets or sets the level in the list, overriding the default behavior of the field. |
| [list_name](./list_name/) | Gets or sets the name of the abstract numbering definition used for the numbering. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [starting_number](./starting_number/) | Gets or sets the starting value for this field. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

