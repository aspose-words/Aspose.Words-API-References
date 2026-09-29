---
title: TxtSaveOptions.preserve_table_layout property
linktitle: preserve_table_layout property
articleTitle: preserve_table_layout property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.preserve_table_layout property. Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format"
type: docs
weight: 60
url: /sv/python-net/aspose.words.saving/txtsaveoptions/preserve_table_layout/
---

## TxtSaveOptions.preserve_table_layout property

Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format.
The default value is ``False``.



```python
@property
def preserve_table_layout(self) -> bool:
    ...

@preserve_table_layout.setter
def preserve_table_layout(self, value: bool):
    ...

```

### Examples

Shows how to preserve the layout of tables when converting to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1')
builder.insert_cell()
builder.write('Row 1, cell 2')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, cell 1')
builder.insert_cell()
builder.write('Row 2, cell 2')
builder.end_table()
# Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur vi sparar dokumentet som klartext.
txt_save_options = aw.saving.TxtSaveOptions()
# Ställ in egenskapen "PreserveTableLayout" till "true" för att applicera mellanslagspadding på innehållet
# i utdata-plaintext-dokumentet för att bevara så mycket av tabellens layout som möjligt.
# Ställ in egenskapen "PreserveTableLayout" till "false" för att spara alla tabellers innehåll
# som en kontinuerlig textmassa, med bara en ny rad för varje rad.
txt_save_options.preserve_table_layout = preserve_table_layout
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PreserveTableLayout.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.PreserveTableLayout.txt')
if preserve_table_layout:
    self.assertEqual('Row 1, cell 1                                            Row 1, cell 2\r\n' + 'Row 2, cell 1                                            Row 2, cell 2\r\n\r\n', doc_text)
else:
    self.assertEqual('Row 1, cell 1\r' + 'Row 1, cell 2\r' + 'Row 2, cell 1\r' + 'Row 2, cell 2\r\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

