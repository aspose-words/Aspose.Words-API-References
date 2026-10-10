---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /zh/python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# BIDIOUTLINE 字段像 AUTONUM/LISTNUM 字段一样为段落编号，
# 但仅在启用从右到左的编辑语言（如希伯来语或阿拉伯语）时可见。
# 以下字段将显示 \".1\"，即列表编号 \"1.\" 的 RTL 等价形式。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# 再添加两个 BIDIOUTLINE 字段，它们将显示 \".2\" 和 \".3\"。
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# 将文档中每个段落的水平文本对齐设置为 RTL。
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# 如果我们在 Microsoft Word 中启用从右到左的编辑语言，我们的字段将显示数字。
# 否则，它们将显示 \"###\"。
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how to detect plaintext document text direction.

```python
# 创建一个 "TxtLoadOptions" 对象，可将其传递给文档的构造函数
# 以修改加载纯文本文档的方式。
load_options = aw.loading.TxtLoadOptions()
# 将 "DocumentDirection" 属性设置为 "DocumentDirection.Auto"，可自动检测
# Aspose.Words 从纯文本加载的每个段落文本的方向。
# 每个段落的 "Bidi" 属性将存储其方向。
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# 将希伯来文检测为从右到左。
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# 将英文检测为从右到左。
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

