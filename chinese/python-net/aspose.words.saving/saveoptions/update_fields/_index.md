---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 150
url: /zh/python-net/aspose.words.saving/saveoptions/update_fields/
---

## SaveOptions.update_fields property

Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format.
Default value for this property is ``True``.



```python
@property
def update_fields(self) -> bool:
    ...

@update_fields.setter
def update_fields(self, value: bool):
    ...

```

### Remarks

Allows to specify whether to mimic or not MS Word behavior.


### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用 PAGE 和 NUMPAGES 字段插入文本。这些字段不会实时显示正确的值。
# 我们需要使用诸如 "Field.Update()" 和 "Document.UpdateFields()" 的更新方法手动更新它们。
# 每次我们需要它们显示准确的值时。
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 将 "UpdateFields" 属性设置为 "false"，以在保存操作之前不更新文档中的所有字段。
# 如果我们知道在保存之前所有字段都是最新的，这是更可取的选项。
# 将 "UpdateFields" 属性设置为 "true"，以遍历整个文档
# 字段并在我们将其保存为 PDF 之前更新它们。这将确保所有字段将显示
# PDF 中最准确的值。
options.update_fields = update_fields
# 我们可以克隆 PdfSaveOptions 对象。
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

