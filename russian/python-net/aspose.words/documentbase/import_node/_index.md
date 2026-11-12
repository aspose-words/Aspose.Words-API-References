---
title: DocumentBase.import_node method
linktitle: import_node method
articleTitle: import_node method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBase.import_node method"
type: docs
weight: 110
url: /ru/python-net/aspose.words/documentbase/import_node/
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
# Каждый узел имеет родительский документ, которым является документ, содержащий узел.
# Вставка узла в документ, к которому узел не принадлежит, вызовет исключение.
src_doc = aw.Document()
dst_doc = aw.Document()
src_doc.first_section.body.first_paragraph.append_child(aw.Run(doc=src_doc, text='Source document first paragraph text.'))
dst_doc.first_section.body.first_paragraph.append_child(aw.Run(doc=dst_doc, text='Destination document first paragraph text.'))
self.assertNotEqual(dst_doc, src_doc.first_section.document)
# Используйте метод ImportNode, чтобы создать копию узла, который будет иметь документ
# который, вызвавший метод ImportNode, будет установлен в качестве нового владельца документа.
imported_section = dst_doc.import_node(src_node=src_doc.first_section, is_import_children=True).as_section()
self.assertEqual(dst_doc, imported_section.document)
# Теперь мы можем вставить узел в документ.
dst_doc.append_child(imported_section)
self.assertEqual('Destination document first paragraph text.\r\nSource document first paragraph text.\r\n', dst_doc.to_string(save_format=aw.SaveFormat.TEXT))
```

Shows how to import node from source document to destination document with specific options.

```python
# Создайте два документа и добавьте символьный стиль к каждому документу.
# Настройте стили так, чтобы у них было одинаковое имя, но разное форматирование текста.
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
# Импортируйте раздел из целевого документа в исходный документ, вызывая конфликт имён стилей.
# Если мы используем стили назначения, то импортированный исходный текст с тем же именем стиля
# как и текст назначения, будет принимать стиль назначения.
imported_section = dst_doc.import_node(src_node=src_doc.first_section, is_import_children=True, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES).as_section()
self.assertEqual(dst_style.font.name, imported_section.body.first_paragraph.runs[0].font.name)
self.assertEqual(dst_style.name, imported_section.body.first_paragraph.runs[0].font.style_name)
# Если мы используем ImportFormatMode.KeepDifferentStyles, стиль источника сохраняется,
# и конфликт имён решается добавлением суффикса.
dst_doc.import_node(src_node=src_doc.first_section, is_import_children=True, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES)
self.assertEqual(dst_style.font.name, dst_doc.styles.get_by_name('My style').font.name)
self.assertEqual(src_style.font.name, dst_doc.styles.get_by_name('My style_0').font.name)
```

Shows how to import a node with resolving source theme colors of shapes.

```python
src_doc = aw.Document()
builder = aw.DocumentBuilder(doc=src_doc)
# Перейдите к основному колонтитулу и вставьте фигуру, использующую цвета темы.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=50)
shape.stroke.fore_theme_color = aw.themes.ThemeColor.DARK1
dst_doc = aw.Document()
# Импортируйте исходный колонтитул в целевой документ с разрешёнными цветами темы,
# чтобы фигура сохраняла свой фактический цвет из исходного документа.
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

