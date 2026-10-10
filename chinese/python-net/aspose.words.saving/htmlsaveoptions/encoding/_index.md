---
title: HtmlSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML, MHTML or EPUB"
type: docs
weight: 100
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/encoding/
---

## HtmlSaveOptions.encoding property

Specifies the encoding to use when exporting to HTML, MHTML or EPUB.
Default value is ``new UTF8Encoding(false)`` (UTF-8 without BOM).



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Remarks




### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# 使用 SaveOptions 对象指定我们将要保存的文档的编码。
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# 默认情况下，输出的 .epub 文档的所有内容都位于一个 HTML 部分。
# 拆分准则允许我们将文档分割为多个 HTML 部分。
# 我们将设置准则，将文档拆分为标题段落。
# 这对于无法读取大于特定大小的 HTML 文件的阅读器很有用。
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# 指定我们要导出文档属性。
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

