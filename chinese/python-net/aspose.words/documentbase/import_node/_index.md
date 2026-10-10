---
title: DocumentBase.import_node method
linktitle: import_node method
articleTitle: import_node method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBase.import_node method"
type: docs
weight: 110
url: /zh/python-net/aspose.words/documentbase/import_node/
---

## import_node(src_node, is_import_children) {#node_bool}

Imports a node from another document to the current document.




```python
def import_node(self, src_node: aspose.words.Node, is_import_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_node | [Node](../../node/) | The node being imported. |
| is_import_children | bool | ``True`` to import all child nodes recursively; otherwise, ``False``. |

### Remarks

This method uses the [ImportFormatMode.USE_DESTINATION_STYLES](../../importformatmode/#USE_DESTINATION_STYLES) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node) or 
[CompositeNode.insert_after()](../../compositenode/insert_after/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned node that belongs to the current document.


## import_node(src_node, is_import_children, import_format_mode) {#node_bool_importformatmode}

Imports a node from another document to the current document with an option to control formatting.




```python
def import_node(self, src_node: aspose.words.Node, is_import_children: bool, import_format_mode: aspose.words.ImportFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_node | [Node](../../node/) | The node to imported. |
| is_import_children | bool | ``True`` to import all child nodes recursively; otherwise, ``False``. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

### Remarks

This overload is useful to control how styles and list formatting are imported.

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node) or 
[CompositeNode.insert_after()](../../compositenode/insert_after/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned, imported node. The node belongs to the destination document, but has no parent.


## import_node(src_node, is_import_children, import_format_mode, import_format_options) {#node_bool_importformatmode_importformatoptions}

Imports a node from another document to the current document with an option to control formatting.




```python
def import_node(self, src_node: aspose.words.Node, is_import_children: bool, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_node | [Node](../../node/) | The node to imported. |
| is_import_children | bool | ``True`` to import all child nodes recursively; otherwise, ``False``. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) | Allows to specify various additional formating options. |

### Remarks

This overload is useful to control how styles and list formatting are imported.

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node) or 
[CompositeNode.insert_after()](../../compositenode/insert_after/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned, imported node. The node belongs to the destination document, but has no parent.


## Examples

Shows how to import a node from one document to another.

```python
# 每个节点都有一个父文档，即包含该节点的文档。
# 将节点插入不属于该节点的文档会抛出异常。
src_doc = aw.Document()
dst_doc = aw.Document()
src_doc.first_section.body.first_paragraph.append_child(aw.Run(doc=src_doc, text='Source document first paragraph text.'))
dst_doc.first_section.body.first_paragraph.append_child(aw.Run(doc=dst_doc, text='Destination document first paragraph text.'))
self.assertNotEqual(dst_doc, src_doc.first_section.document)
# 使用 ImportNode 方法创建节点的副本，该副本将拥有文档
# 调用 ImportNode 方法的文档将被设置为其新的所有者文档。
imported_section = dst_doc.import_node(src_node=src_doc.first_section, is_import_children=True).as_section()
self.assertEqual(dst_doc, imported_section.document)
# 我们现在可以将节点插入文档。
dst_doc.append_child(imported_section)
self.assertEqual('Destination document first paragraph text.\r\nSource document first paragraph text.\r\n', dst_doc.to_string(save_format=aw.SaveFormat.TEXT))
```

Shows how to import node from source document to destination document with specific options.

```python
# 创建两个文档，并为每个文档添加字符样式。
# 配置样式，使其具有相同的名称，但不同的文本格式。
src_doc = aw.Document()
src_style = src_doc.styles.add(aw.StyleType.CHARACTER, 'My style')
src_style.font.name = 'Courier New'
src_builder = aw.DocumentBuilder(doc=src_doc)
src_builder.font.style = src_style
src_builder.writeln('Source document text.')
dst_doc = aw.Document()
dst_style = dst_doc.styles.add(aw.StyleType.CHARACTER, 'My style')
dst_style.font.name = 'Calibri'
dst_builder = aw.DocumentBuilder(doc=dst_doc)
dst_builder.font.style = dst_style
dst_builder.writeln('Destination document text.')
# 将目标文档中的 Section 导入到源文档，导致样式名称冲突。
# 如果使用目标样式，则导入的源文本使用相同的样式名称
# 将采用目标样式。
imported_section = dst_doc.import_node(src_node=src_doc.first_section, is_import_children=True, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES).as_section()
self.assertEqual(dst_style.font.name, imported_section.body.first_paragraph.runs[0].font.name)
self.assertEqual(dst_style.name, imported_section.body.first_paragraph.runs[0].font.style_name)
# 如果使用 ImportFormatMode.KeepDifferentStyles，源样式将被保留，
# 并通过添加后缀来解决命名冲突。
dst_doc.import_node(src_node=src_doc.first_section, is_import_children=True, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES)
self.assertEqual(dst_style.font.name, dst_doc.styles.get_by_name('My style').font.name)
self.assertEqual(src_style.font.name, dst_doc.styles.get_by_name('My style_0').font.name)
```

Shows how to import a node with resolving source theme colors of shapes.

```python
src_doc = aw.Document()
builder = aw.DocumentBuilder(doc=src_doc)
# 移动到主页脚并插入使用主题颜色的形状。
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=50)
shape.stroke.fore_theme_color = aw.themes.ThemeColor.DARK1
dst_doc = aw.Document()
# 将源页脚导入目标文档，并解析主题颜色，
# 使该形状保留来自源文档的实际颜色。
footer = src_doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.ImportFormatOptions()
options.resolve_theme_colors = True
imported_footer = dst_doc.import_node(src_node=footer, is_import_children=True, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options).as_header_footer()
dst_doc.first_section.headers_footers.add(imported_footer)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.ImportNodeWithResolveThemeColors.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [NodeImporter](../../nodeimporter/)
* enum [ImportFormatMode](../../importformatmode/)

