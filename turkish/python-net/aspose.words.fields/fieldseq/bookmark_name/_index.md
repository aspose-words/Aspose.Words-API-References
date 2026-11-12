---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldseq/bookmark_name/
---

## FieldSeq.bookmark_name property

Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
# Her giriş, SEQ alanını içeren paragrafı içerir,
# ve alanın göründüğü sayfanın numarasını.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Bu TOC alanını, değeri "MySequence" olan bir SequenceIdentifier özelliğine sahip olacak şekilde yapılandırın.
field_toc.table_of_figures_label = 'MySequence'
# Bu TOC alanını, yalnızca bir yer iminin sınırları içinde olan SEQ alanlarını alacak şekilde yapılandırın
# "TOCBookmark" adlı.
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ alanları, her SEQ alanında artan bir sayım gösterir.
# Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar
# SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanan.
# TOC'nin eşleşen bir sıra tanımlayıcısına sahip bir SEQ alanı ekleyin
# TableOfFiguresLabel özelliği. Bu alan, dışarıda olduğu için TOC'de bir giriş oluşturmayacaktır
# "BookmarkName" tarafından belirlenen yer imi sınırları.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# Bu SEQ alanının sırası, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşir ve yer imi sınırları içindedir.
# Bu alanı içeren paragraf, TOC'de bir giriş olarak görünecektir.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# Bu SEQ alanının sırası, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşmez,
# ve yer imi sınırları içindedir. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# Bu SEQ alanının sırası, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşir ve yer imi sınırları içindedir.
# Bu alan ayrıca başka bir yer imine referans verir. O yer iminin içeriği, bu SEQ alanı için TOC girişinde görünecektir.
# SEQ alanı kendisi o yer iminin içeriğini görüntülemeyecektir.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Yukarıdaki SEQ alanının ona referans vermesi nedeniyle TOC girişinde görünecek içeriklere sahip bir yer imi oluşturun.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

