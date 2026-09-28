---
title: XpsSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/xpssaveoptions/use_book_fold_printing_settings/
---

## XpsSaveOptions.use_book_fold_printing_settings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout,
if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/).



```python
@property
def use_book_fold_printing_settings(self) -> bool:
    ...

@use_book_fold_printing_settings.setter
def use_book_fold_printing_settings(self, value: bool):
    ...

```

### Remarks

If this option is specified, [FixedPageSaveOptions.page_set](../../fixedpagesaveoptions/page_set/) is ignored when saving.
This behavior matches MS Word.
If book fold printing settings are not specified in page setup, this option will have no effect.





### Examples

Shows how to save a document to the XPS format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# 创建一个 "XpsSaveOptions" 对象，以便我们可以将其传递给文档的 "Save" 方法
# 以修改该方法将文档转换为 .XPS 的方式。
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# 将 "UseBookFoldPrintingSettings" 属性设置为 "true"，以排列内容
# 在输出的 XPS 中，以有助于我们将其制成小册子的方式。
# 将 "UseBookFoldPrintingSettings" 属性设置为 "false" 以正常渲染 XPS。
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# 如果我们将文档渲染为小册子，则必须设置 "MultiplePages"
# 所有节的页面设置对象的属性设置为 "MultiplePagesType.BookFoldPrinting"。
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# 一旦我们打印此文档，就可以通过堆叠页面将其制成小册子
# 让它们从打印机出来后在中间折叠。
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

