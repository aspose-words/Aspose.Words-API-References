---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/pssaveoptions/save_format/
---

## PsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.PS](../../../aspose.words/saveformat/#PS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to the Postscript format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# 创建一个 "PsSaveOptions" 对象，以便我们可以将其传递给文档的 "Save" 方法
# 以修改该方法将文档转换为 PostScript 的方式。
# 将 "UseBookFoldPrintingSettings" 属性设置为 "true"，以排列内容
# 在输出的 Postscript 文档中，以帮助我们将其制成小册子的方式进行排列。
# 将 "UseBookFoldPrintingSettings" 属性设置为 "false"，以正常保存文档。
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# 如果我们将文档渲染为小册子，则必须设置 "MultiplePages"
# 所有节的页面设置对象的属性设置为 "MultiplePagesType.BookFoldPrinting"。
for s in doc.sections:
    s = s.as_section()
    s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# 一旦我们在页面的两面打印此文档，就可以一次性将所有页面在中间对折，
# 并且内容会对齐，从而形成小册子。
doc.save(file_name=ARTIFACTS_DIR + 'PsSaveOptions.UseBookFoldPrintingSettings.ps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

