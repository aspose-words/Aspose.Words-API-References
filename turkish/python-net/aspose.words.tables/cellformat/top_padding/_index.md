---
title: CellFormat.top_padding property
linktitle: top_padding property
articleTitle: top_padding property
second_title: Aspose.Words for Python
description: "CellFormat.top_padding property. Returns or sets the amount of space (in points) to add above the contents of cell."
type: docs
weight: 110
url: /tr/python-net/aspose.words.tables/cellformat/top_padding/
---

## CellFormat.top_padding property

Returns or sets the amount of space (in points) to add above the contents of cell.


```python
@property
def top_padding(self) -> float:
    ...

@top_padding.setter
def top_padding(self, value: float):
    ...

```

### Examples

Shows how to format cells with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# İkinci bir hücre ekleyin ve ardından hücre metni doldurma seçeneklerini yapılandırın.
# Builder bu ayarları mevcut hücresine uygular ve sonradan oluşturulan tüm yeni hücreler de bu ayarları alır.
builder.insert_cell()
cell_format = builder.cell_format
cell_format.width = 250
cell_format.left_padding = 30
cell_format.right_padding = 30
cell_format.top_padding = 30
cell_format.bottom_padding = 30
builder.write('Row 1, cell 2.')
builder.end_row()
builder.end_table()
# İlk hücre, doldurma yeniden yapılandırmasından etkilenmemiştir ve hâlâ varsayılan değerleri tutmaktadır.
self.assertEqual(0, table.first_row.cells[0].cell_format.width)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.left_padding)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.right_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.top_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.bottom_padding)
self.assertEqual(250, table.first_row.cells[1].cell_format.width)
self.assertEqual(30, table.first_row.cells[1].cell_format.left_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.right_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.top_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.bottom_padding)
# İlk hücre, çıktı belgesinde komşu hücrenin boyutuna eşit olacak şekilde yine de büyümeye devam edecektir.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetCellFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

