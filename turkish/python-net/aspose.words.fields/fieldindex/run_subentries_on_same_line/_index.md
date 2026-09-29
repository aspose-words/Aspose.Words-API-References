---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /tr/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# INDEX girdisi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacak
# her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişe.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# Text özelliği değeri INDEX girişinin başlığı haline gelen XE alanları.
# Bu değer iki dizge segmenti içeriyorsa ve iki nokta üst üste ile bölünmüşse (INDEX girişi :) ayırıcıyı işleyecek,
# ilk segment başlık, ikinci segment ise alt başlık olacaktır.
# INDEX alanı önce girişleri alfabetik olarak gruplar, ardından aynı
# başlıklara sahip birden fazla XE alanı varsa, INDEX alanı bunları bu başlıkların değerlerine göre daha da alt gruplara ayıracaktır.
# Kaç kez
# XE alanlarının Text özellikleri bu şekilde bölündüğüne bağlı olarak birden fazla alt gruplama katmanı olabilir.
# Varsayılan olarak, bir INDEX alanı giriş grubu bu grup içindeki her alt başlık için yeni bir satır oluşturur.
# Başlığı korumak için RunSubentriesOnSameLine bayrağını true olarak ayarlayabiliriz,
# ve grup için tüm alt başlıkları tek bir satırda tutar, bu da INDEX alanını daha kompakt hale getirir.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# İki XE alanı ekleyin, her biri yeni bir sayfada ve aynı "Heading 1" başlığına sahip,
# ki bu, INDEX alanının onları gruplamak için kullanacağıdır.
# RunSubentriesOnSameLine false ise, INDEX tablosu üç satır oluşturur:
# "Heading 1" gruplama başlığı için bir satır ve her alt başlık için bir satır daha.
# RunSubentriesOnSameLine true ise, INDEX tablosu tek satırlık bir
# giriş oluşturur; bu giriş başlığı ve tüm alt başlıkları kapsar.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

