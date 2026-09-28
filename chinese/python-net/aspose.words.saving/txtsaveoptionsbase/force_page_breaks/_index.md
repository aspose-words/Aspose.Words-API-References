---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
---

## TxtSaveOptionsBase.force_page_breaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is ``False``.




```python
@property
def force_page_breaks(self) -> bool:
    ...

@force_page_breaks.setter
def force_page_breaks(self, value: bool):
    ...

```

### Remarks

The property affects only page breaks that are inserted explicitly into a document. 
It is not related to page breaks that MS Word automatically inserts at the end of each page.


### Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3')
# 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 用于修改我们将文档保存为纯文本的方式的方法。
save_options = aw.saving.TxtSaveOptions()
# Aspose.Words 的 "Document" 对象具有分页符，就像 Microsoft Word 文档一样。
# 保存格式，例如 ".txt"，是一段连续的文本，没有分页符。
# 将 "ForcePageBreaks" 属性设置为 "true"，以保留所有以 '\f' 字符形式存在的分页符。
# 将 "ForcePageBreaks" 属性设置为 "false"，以丢弃所有分页符。
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# 如果我们加载带有分页符的纯文本文档，
# "Document" 对象将使用它们将正文拆分为多个页面。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

