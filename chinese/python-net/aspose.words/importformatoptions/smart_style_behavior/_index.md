---
title: ImportFormatOptions.smart_style_behavior property
linktitle: smart_style_behavior property
articleTitle: smart_style_behavior property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.smart_style_behavior property. Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents"
type: docs
weight: 100
url: /zh/python-net/aspose.words/importformatoptions/smart_style_behavior/
---

## ImportFormatOptions.smart_style_behavior property

Gets or sets a boolean value that specifies how styles will be imported
when they have equal names in source and destination documents.
The default value is ``False``.



```python
@property
def smart_style_behavior(self) -> bool:
    ...

@smart_style_behavior.setter
def smart_style_behavior(self, value: bool):
    ...

```

### Remarks

When this option is **enabled**, the source style will be expanded into a direct attributes inside a
destination document, if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing
destination attributes will not be overridden, including lists.




### Examples

Shows how to resolve duplicate styles while inserting documents.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
my_style = builder.document.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
my_style.font.size = 14
my_style.font.name = 'Courier New'
my_style.font.color = aspose.pydrawing.Color.blue
builder.paragraph_format.style_name = my_style.name
builder.writeln('Hello world!')
# 克隆文档并编辑克隆的 "MyStyle" 样式，使其颜色与原始文档不同。
# 如果我们将克隆插入原始文档，两个同名样式将导致冲突。
src_doc = dst_doc.clone()
src_doc.styles.get_by_name('MyStyle').font.color = aspose.pydrawing.Color.red
# 当我们启用 SmartStyleBehavior 并使用 KeepSourceFormatting 导入格式模式时，
# Aspose.Words 将通过转换源文档样式来解决样式冲突。
# 将与目标样式同名的样式转换为直接的段落属性。
options = aw.ImportFormatOptions()
options.smart_style_behavior = True
builder.insert_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SmartStyleBehavior.docx')
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

