---
title: FieldToc.table_of_figures_label property
linktitle: table_of_figures_label property
articleTitle: table_of_figures_label property
second_title: Aspose.Words for Python
description: "FieldToc.table_of_figures_label property. Gets or sets the name of the sequence identifier used when building a table of figures."
type: docs
weight: 160
url: /tr/python-net/aspose.words.fields/fieldtoc/table_of_figures_label/
---

## FieldToc.table_of_figures_label property

Gets or sets the name of the sequence identifier used when building a table of figures.


```python
@property
def table_of_figures_label(self) -> str:
    ...

@table_of_figures_label.setter
def table_of_figures_label(self, value: str):
    ...

```

### Examples

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
# Her giriş, SEQ alanını içeren paragrafı ve alanın göründüğü sayfanın numarasını içerir.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ alanları, her SEQ alanında artan bir sayım gösterir.
# Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar
# SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanan.
# TOC için ana bir dizi adlandırmak üzere "TableOfFiguresLabel" özelliğini kullanın.
# Şimdi, bu TOC yalnızca "SequenceIdentifier" özelliği "MySequence" olarak ayarlanmış SEQ alanlarından giriş oluşturacaktır.
field_toc.table_of_figures_label = 'MySequence'
# "PrefixedSequenceIdentifier" özelliğinde başka bir SEQ alanı dizisi adlandırabiliriz.
# Bu önek dizisindeki SEQ alanları TOC girişleri oluşturmayacaktır.
# Ana dizi SEQ alanından oluşturulan her TOC girişi artık sayımı da gösterecek
# ön ek sırası şu anda girişin oluşturulduğu birincil sıra SEQ alanında bulunuyor.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Her TOC girişi, ön ek sırası sayısını hemen solunda gösterecek
# ana sıra SEQ alanının bulunduğu sayfa numarasının
# Bu iki sayı arasında görünecek özel bir ayırıcı belirleyebiliriz.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Bu TOC'yi doldurmak için SEQ alanlarını kullanmanın iki yolu vardır.
# 1 -  TOC'nun ön ek sırasına ait bir SEQ alanı eklemek:
# Bu alan, "PrefixSequence" için SEQ sıra sayacını 1 artıracaktır.
# Bu alan, tanımlanan ana sıraya ait olmadığı için
# TOC'nin "TableOfFiguresLabel" özelliği tarafından belirlenen, bir giriş olarak görünmeyecektir.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  TOC'nun ana sırasına ait bir SEQ alanı eklemek:
# Bu SEQ alanı TOC'de bir giriş oluşturacaktır.
# TOC girişi, SEQ alanının bulunduğu paragrafı ve onun göründüğü sayfa numarasını içerecek.
# Bu giriş ayrıca ön ek sırasının şu anda bulunduğu sayıyı da gösterecek,
# sayfa numarasından, TOC'nin SeqenceSeparator özelliğindeki değerle ayrılmış olarak.
# "PrefixSequence" sayacı 1'de, bu ana sıra SEQ alanı sayfa 2'de,
# ve ayırıcı ">" olduğundan, giriş "1>2" olarak gösterilecek.
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Bir sayfa ekleyin, ön ek sırasını 2 artırın ve ardından bir SEQ alanı ekleyerek TOC girişini oluşturun.
# Ön ek sırası artık 2'de, ve ana sıra SEQ alanı sayfa 3'te,
# bu yüzden TOC girişi sayfa sayısında "2>3" olarak gösterilecek.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

