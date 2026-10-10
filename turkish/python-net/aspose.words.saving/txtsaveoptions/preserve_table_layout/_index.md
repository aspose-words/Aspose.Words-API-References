---
title: TxtSaveOptions.preserve_table_layout property
linktitle: preserve_table_layout property
articleTitle: preserve_table_layout property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.preserve_table_layout property. Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format"
type: docs
weight: 60
url: /tr/python-net/aspose.words.saving/txtsaveoptions/preserve_table_layout/
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
# "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" metoduna geçirebiliriz
# belgeyi düz metin olarak nasıl kaydedeceğimizi değiştirmek için.
txt_save_options = aw.saving.TxtSaveOptions()
# "PreserveTableLayout" özelliğini "true" olarak ayarlayarak içeriğe boşluk dolgusu uygulayın
# çıktı düz metin belgesinin tablo düzeninin mümkün olduğunca çok kısmını korumak için.
# "PreserveTableLayout" özelliğini "false" olarak ayarlayarak tüm tabloların içeriğini kaydedin
# her satır için sadece yeni bir satırla, kesintisiz bir metin gövdesi olarak.
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

