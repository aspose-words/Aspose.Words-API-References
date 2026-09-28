---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

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

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# 打开一个在 Microsoft Word 2003 中创建的文档。
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# 如果我们打开 Word 文档并按 Alt+F9，就会看到一个 SHAPE 字段和一个 EMBED 字段。
# SHAPE 字段是带有“与文字同行”换行样式的 AutoShape 对象的锚点/画布。
# EMBED 字段具有相同的功能，但用于嵌入的对象，
# 例如来自外部 Excel 文档的电子表格。
# 然而，这些字段不会出现在文档的 Fields 集合中。
self.assertEqual(0, doc.range.fields.count)
# 这些字段仅在旧版本的 Microsoft Word 中受支持。
# 文档加载过程会将这些字段转换为 Shape 对象，
# 我们可以在文档的节点集合中访问它们。
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# 第一个 Shape 节点对应于输入文档中的 SHAPE 字段，
# 它是 AutoShape 的行内画布。
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# 第二个 Shape 节点就是 AutoShape 本身。
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# 第三个 Shape 是原先包含外部电子表格的 EMBED 字段。
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

