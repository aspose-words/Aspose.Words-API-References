---
title: CellFormat.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "CellFormat.width property. Gets the width of the cell in points."
type: docs
weight: 140
url: /tr/python-net/aspose.words.tables/cellformat/width/
---

## CellFormat.width property

Gets the width of the cell in points.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
    ...

```

### Remarks

The width is calculated by Aspose.Words on document loading and saving.
Currently, not every combination of table, cell and document properties is supported.
The returned value may not be accurate for some documents.
It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended.
There is no guarantee that the cell will actually have the set width.
The width may be adjusted to accommodate cell contents in an auto-fit table layout.
Cells in other rows may have conflicting width settings.
The table may be resized to fit into the container or to meet table width settings.
Consider using [CellFormat.preferred_width](../preferred_width/) for setting the cell width.
Setting this property sets [CellFormat.preferred_width](../preferred_width/) implicitly since version 15.8.





### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
# bunu eklediğimiz her satır ve hücreye uygulayacaktır.
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True
builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = aspose.pydrawing.Color.orange
builder.insert_cell()
builder.write('Row 1, Col 1')
builder.insert_cell()
builder.write('Row 1, Col 2')
builder.end_row()
# Biçimlendirmeyi değiştirmek, mevcut hücreye uygulanacaktır,
# ve oluşturucu ile daha sonra oluşturduğumuz yeni hücreler.
# Bu, daha önce eklediğimiz hücreleri etkilemez.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Dikey metne sığması için satır yüksekliğini artırın.
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 3, Col 1')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 3, Col 2')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTable.docx')
```

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
* property [CellFormat.preferred_width](../preferred_width/)

