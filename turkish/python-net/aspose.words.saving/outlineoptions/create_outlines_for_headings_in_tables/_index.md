---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /tr/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
---

## OutlineOptions.create_outlines_for_headings_in_tables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```python
@property
def create_outlines_for_headings_in_tables(self) -> bool:
    ...

@create_outlines_for_headings_in_tables.setter
def create_outlines_for_headings_in_tables(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Üç satırlı bir tablo oluşturun. İlk satır,
# metni başlık tipi bir stil ile biçimlendireceğimiz, sütun başlığı olarak hizmet edecektir.
builder.start_table()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('Customers')
builder.end_row()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.write('John Doe')
builder.end_row()
builder.insert_cell()
builder.write('Jane Doe')
builder.end_table()
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
pdf_save_options = aw.saving.PdfSaveOptions()
# Çıktı PDF belgesi bir anahat içerecek; bu, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosudur.
# Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürecek.
# "HeadingsOutlineLevels" özelliğini "1" olarak ayarlayın, taslağı elde etmek için
# yalnızca başlık seviyesi 1'den büyük olmayan başlıkları kaydetmek için.
pdf_save_options.outline_options.headings_outline_levels = 1
# "CreateOutlinesForHeadingsInTables" özelliğini "false" olarak ayarlayın, tablolardaki tüm başlıkları dışlamak için,
# örneğin yukarıda taslaktan oluşturduğumuz gibi.
# "CreateOutlinesForHeadingsInTables" özelliğini "true" olarak ayarlayın, tablolardaki tüm başlıkları dahil etmek için
# taslakta, başlık seviyeleri "HeadingsOutlineLevels" özelliğinin değerinden büyük olmayan sürece.
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

