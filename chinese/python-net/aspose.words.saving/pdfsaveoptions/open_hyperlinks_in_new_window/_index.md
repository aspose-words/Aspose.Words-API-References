---
title: PdfSaveOptions.open_hyperlinks_in_new_window property
linktitle: open_hyperlinks_in_new_window property
articleTitle: open_hyperlinks_in_new_window property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.open_hyperlinks_in_new_window property. Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser."
type: docs
weight: 250
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/open_hyperlinks_in_new_window/
---

## PdfSaveOptions.open_hyperlinks_in_new_window property

Gets or sets a value determining whether hyperlinks in the output Pdf document
are forced to be opened in a new window (or tab) of a browser.


```python
@property
def open_hyperlinks_in_new_window(self) -> bool:
    ...

@open_hyperlinks_in_new_window.setter
def open_hyperlinks_in_new_window(self, value: bool):
    ...

```

### Remarks

The default value is ``False``. When this value is set to ``True``
hyperlinks are saved using JavaScript code.
JavaScript code is ``app.launchURL("URL", true);``,
where ``URL`` is a hyperlink.


Note that if this option is set to ``True`` hyperlinks can't work
in some PDF readers e.g. Chrome, Firefox.


JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance.
The ``False`` value will be used automatically in this case.




### Examples

Shows how to save hyperlinks in a document we convert to PDF so that they open new pages when we click on them.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_hyperlink('Testlink', 'https://www.google.com/search?q=%20aspose', False)
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 将 "OpenHyperlinksInNewWindow" 属性设置为 "true" 以使用 Javascript 代码保存所有超链接
# 使阅读器在新窗口/浏览器标签页中打开这些链接。
# 将 "OpenHyperlinksInNewWindow" 属性设置为 "false" 以正常保存所有超链接。
options.open_hyperlinks_in_new_window = open_hyperlinks_in_new_window
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.OpenHyperlinksInNewWindow.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

