---
title: FieldIndex.has_sequence_name property
linktitle: has_sequence_name property
articleTitle: has_sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.has_sequence_name property. Gets a value indicating whether a sequence should be used while the field's result building."
type: docs
weight: 60
url: /tr/python-net/aspose.words.fields/fieldindex/has_sequence_name/
---

## FieldIndex.has_sequence_name property

Gets a value indicating whether a sequence should be used while the field's result building.


```python
@property
def has_sequence_name(self) -> bool:
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# XE alanlarının "Text" property değerinde aynı değere sahip olması durumunda,
# INDEX alanı bunları tek bir girişte gruplayacaktır.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# SequenceName özelliğinde bir SEQ alanı dizisi adlandırın. Bu INDEX alanının her girişi artık ayrıca görüntüleyecek
# bu girişi oluşturan XE alanı konumundaki dizi sayacının numarasını.
index.sequence_name = 'MySequence'
# Kullanıcıya anlamlarını açıklamak için dizi ve sayfa numaralarının etrafında olacak metni ayarlayın.
# Bu yapılandırmayla oluşturulan bir giriş, sayfa numarasına "MySequence at 1 on page 1" benzeri bir şey gösterecek.
# PageNumberSeparator ve SequenceSeparator 15 karakterden uzun olamaz.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# SEQ alanları, her SEQ alanında artan bir sayım gösterir.
# Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar
# SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanan.
# "MySequence" dizisini 1'e taşıyan bir SEQ alanı ekleyin.
# Bu alan normal belge metninden farklı değildir. Bir INDEX alanının içindekiler tablosunda görünmez.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# INDEX alanında bir giriş oluşturacak bir XE alanı ekleyin.
# "MySequence" 1'de ve bu XE alanı sayfa 2'de olduğundan, yukarıda tanımladığımız özel ayırıcılarla birlikte,
# bu alanın INDEX girişi sol tarafta "Cat", sağ tarafta ise "MySequence at 1 on page 2" gösterecek.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Bir sayfa sonu ekleyin ve "MySequence"'i 3'e ilerletmek için SEQ alanlarını kullanın.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Yukarıdakiyle aynı Text özelliğine sahip bir XE alanı ekleyin.
# INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip XE alanlarını gruplayacaktır
# her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişe.
# Sayfa 2'de "MySequence" 3 olduğundan, ", 3 on page 3" aynı INDEX girişine yukarıdaki gibi eklenecek.
# Bu INDEX girişinin sayfa numarası kısmı artık "MySequence at 1 on page 2, 3 on page 3" gösterecek.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Yeni ve benzersiz bir Text özelliği değeriyle bir XE alanı ekleyin.
# Bu, sayfa 4'te MySequence 3 olan yeni bir giriş ekleyecek.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

