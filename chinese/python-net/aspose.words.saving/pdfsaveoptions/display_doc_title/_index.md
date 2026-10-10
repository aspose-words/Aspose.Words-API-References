---
title: PdfSaveOptions.display_doc_title property
linktitle: display_doc_title property
articleTitle: display_doc_title property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.display_doc_title property. A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary."
type: docs
weight: 90
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/display_doc_title/
---

## PdfSaveOptions.display_doc_title property

A flag specifying whether the window’s title bar should display the document title taken from
the Title entry of the document information dictionary.


```python
@property
def display_doc_title(self) -> bool:
    ...

@display_doc_title.setter
def display_doc_title(self, value: bool):
    ...

```

### Remarks

If ``False``, the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance. ``True`` value will be used automatically when saving
to PDF/UA.

The default value is ``False``.




### Examples

Shows how to display the title of the document as the title bar.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
doc.built_in_document_properties.title = 'Windows bar pdf title'
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
# 将 "DisplayDocTitle" 设置为 "true"，可让某些 PDF 阅读器（如 Adobe Acrobat Pro）
# 在属于该文档的标签页中显示文档的内置属性 "Title" 的值。
# 将 "DisplayDocTitle" 设置为 "false"，使这些阅读器显示文档的文件名。
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.display_doc_title = display_doc_title
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DocTitle.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

