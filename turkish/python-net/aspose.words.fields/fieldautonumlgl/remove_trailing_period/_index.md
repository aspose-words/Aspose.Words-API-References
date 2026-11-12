---
title: FieldAutoNumLgl.remove_trailing_period property
linktitle: remove_trailing_period property
articleTitle: remove_trailing_period property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.remove_trailing_period property. Gets or sets whether to display the number without a trailing period."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldautonumlgl/remove_trailing_period/
---

## FieldAutoNumLgl.remove_trailing_period property

Gets or sets whether to display the number without a trailing period.


```python
@property
def remove_trailing_period(self) -> bool:
    ...

@remove_trailing_period.setter
def remove_trailing_period(self, value: bool):
    ...

```

### Examples

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# AUTONUMLGL alanları, mevcut başlık seviyesindeki her AUTONUMLGL alanında artan bir sayı gösterir.
# Bu alanlar her başlık seviyesi için ayrı bir sayım tutar,
# ve her alan ayrıca kendi seviyesinin altındaki tüm başlık seviyeleri için AUTONUMLGL alan sayımlarını da gösterir.
# Herhangi bir başlık seviyesinin sayısını değiştirmek, o seviyenin üzerindeki tüm seviyelerin sayısını 1'e sıfırlar.
# Bu, belgemizi bir taslak listesi biçiminde düzenlememizi sağlar.
# Bu, 1. başlık seviyesinde ilk AUTONUMLGL alanıdır ve belgede "1." gösterir.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Bu, 1. başlık seviyesinde ikinci AUTONUMLGL alanıdır, bu yüzden "2." gösterir.
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Bu, 2. başlık seviyesinde ilk AUTONUMLGL alanıdır,
# ve altındaki başlık seviyesinin AUTONUMLGL sayısı "2" olduğundan, "2.1." gösterir.
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Bu, 3. başlık seviyesinde ilk AUTONUMLGL alanıdır.
# Yukarıdaki alanla aynı şekilde çalışarak "2.1.1." gösterir.
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Bu alan 2. başlık seviyesindedir ve ilgili AUTONUMLGL sayısı 2 olduğundan, alan "2.2." gösterir.
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Bu seviyenin altındaki bir başlık seviyesi için AUTONUMLGL sayısını artırmak
# bu seviyenin sayısını sıfırlamış ve bu alanın "2.2.1." göstermesini sağlamıştır.
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # Sayıdan hemen sonra alan sonucunda görünen ayırıcı karakter,
    # varsayılan olarak bir nokta sonudur. Bu özelliği null bırakırsak,
    # son AUTONUMLGL alanımız belgede "2.2.1." gösterecektir.
    self.assertIsNone(field.separator_character)
    # Özel bir ayırıcı karakter ayarlamak ve son nokta işaretini kaldırmak
    # alanın görünümünü "2.2.1." yerine "2:2:1" olarak değiştirecektir.
    # Bunu oluşturduğumuz tüm alanlara uygulayacağız.
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # Bu metin, üzerindeki otomatik numaralı yasal alana ait olacaktır.
    # Microsoft Word'de ilgili AUTONUMLGL alanının yanındaki oka tıkladığımızda daralacaktır.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

