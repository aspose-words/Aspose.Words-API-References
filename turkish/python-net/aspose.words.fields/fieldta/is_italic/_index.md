---
title: FieldTA.is_italic property
linktitle: is_italic property
articleTitle: is_italic property
second_title: Aspose.Words for Python
description: "FieldTA.is_italic property. Gets or sets whether to apply italic formatting to the page number for the entry."
type: docs
weight: 40
url: /tr/python-net/aspose.words.fields/fieldta/is_italic/
---

## FieldTA.is_italic property

Gets or sets whether to apply italic formatting to the page number for the entry.


```python
@property
def is_italic(self) -> bool:
    ...

@is_italic.setter
def is_italic(self, value: bool):
    ...

```

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgedeki her TA alanı için bir giriş oluşturacak bir TOA alanı ekleyin,
# her giriş için uzun atıfları ve sayfa numaralarını gösterir.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Tablomuz için giriş kategorisini ayarlayın. Bu TOA artık yalnızca TA alanlarını içerir
# EntryCategory özelliklerinde eşleşen bir değere sahip olanları.
field_toa.entry_category = '1'
# Ayrıca, Yetki Tablosu kategorisi indeks 1'de "Cases" olarak belirlenmiştir,
# bu değişkeni true olarak ayarlarsak tablomuzun başlığı olarak görünecek.
field_toa.use_heading = True
# TA alanlarını, TOA sınırları içinde olmaları gereken bir yer imi adı vererek daha da filtreleyebiliriz.
field_toa.bookmark_name = 'MyBookmark'
# Varsayılan olarak, TA alanının atıfı ile
# sayfa numarası arasında sayfa genişliğinde noktalı bir sekme görünür. Bu sekmeyi bu özelliğe koyduğumuz herhangi bir metinle değiştirebiliriz.
# Bir sekme karakteri eklemek orijinal sekmeyi korur.
field_toa.entry_separator = ' \t p.'
# Aynı uzun atıfa sahip birden fazla TA girişi varsa,
# tüm ilgili sayfa numaraları tek bir satırda gösterilir.
# Bu özelliği, sayfa numaralarını ayıracak bir dize belirtmek için kullanabiliriz.
field_toa.page_number_list_separator = ' & p. '
# Bunu true olarak ayarlayarak tablomuzun "passim" kelimesini göstermesini sağlayabiliriz.
# bir satırda beş veya daha fazla sayfa numarası varsa.
field_toa.use_passim = True
# Bir TA alanı bir dizi sayfaya referans verebilir.
# Bu tür aralıklar için başlangıç ve bitiş sayfa numaraları arasında görünecek bir dizeyi burada belirtebiliriz.
field_toa.page_range_separator = ' to '
# TA alanlarından gelen format tablomuzda da kullanılacak.
# RemoveEntryFormatting bayrağını ayarlayarak bunu devre dışı bırakabiliriz.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Bu TA alanı, dışarıda olduğu için TOA'da bir giriş olarak görünmeyecek
# TOA'nın BookmarkName özelliğinin belirttiği yer işareti sınırlarının dışındadır.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Bu TA alanı yer işaretinin içindedir,
# ancak giriş kategorisi tabloyla eşleşmediği için TA alanı onu içermeyecek.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Bu giriş tabloya görünecek.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# Bir TOA tablosu kısa atıfları göstermez,
# ancak bunları, birden fazla TA alanının referans verdiği uzun kaynak adlarına kısaltma olarak kullanabiliriz.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Aşağıdaki özellikleri kullanarak sayfa numarasını kalın/eğik biçimlendirebiliriz.
# Tablomuzu biçimlendirmeyi yok sayacak şekilde ayarlarsak bile bu etkileri göreceğiz.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# TA alanlarını, TOA girişlerinin bir yer işaretinin kapsadığı sayfa aralığına referans vermesini sağlayacak şekilde yapılandırabiliriz.
# Bu girişin, tablomuzda aynı satırı paylaşmak için yukarıdakiyle aynı kaynağa referans olduğunu unutmayın.
# Bu satır, yukarıdaki girişin sayfa numarasını ve bu girişin sayfa aralığını içerecek,
# sayfa numaraları arasındaki tablo sayfa listesi ve sayfa numarası aralık ayırıcılarıyla.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Tablomuzun "Passim" özelliğini etkinleştirdiğimizde, aynı kaynağa sahip 5 veya daha fazla TA girişi olması bunu tetikleyecek.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTA](../)

