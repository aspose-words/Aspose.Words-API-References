---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /tr/python-net/aspose.words.fields/fieldseq/
---

## FieldSeq class

Implements the SEQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Sequentially numbers chapters, tables, figures, and other user-defined lists of items in a document.


**Inheritance:** [FieldSeq](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSeq()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_next_number](./insert_next_number/) | Gets or sets whether to insert the next sequence number for the specified item. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [reset_heading_level](./reset_heading_level/) | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [reset_number](./reset_number/) | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_identifier](./sequence_identifier/) | Gets or sets the name assigned to the series of items that are to be numbered. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
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

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# SEQ alanları, her SEQ alanında artan bir sayım gösterir.
# Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar
# SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanan.
# "MySequence"'in mevcut sayı değerini gösterecek bir SEQ alanı ekleyin,
# "ResetNumber" özelliğini kullanarak 100'e ayarladıktan sonra.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Bu sıradaki bir sonraki sayıyı başka bir SEQ alanı ile gösterin.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Seviye 1 başlık ekleyin.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Aynı sıradan başka bir SEQ alanı ekleyin ve sayacı her başlıkta 1 olarak sıfırlayacak şekilde yapılandırın.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Yukarıdaki başlık seviye 1 başlıktır, bu yüzden bu sıradaki sayaç 1'e sıfırlanır.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Bu dizinin bir sonraki numarasına geçin.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

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

* module [aspose.words.fields](../)
* class [Field](../field/)

