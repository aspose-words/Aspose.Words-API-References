---
title: import_node method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.DocumentBase.import_node method"
type: docs
weight: 100
url: /python-net/aspose.words/documentbase/import_node/
---

## import_node(src_node, is_import_children) {#node_bool}

Imports a node from another document to the current document.




```python
def import_node(self, src_node: aspose.words.Node, is_import_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_node | [Node](../../node/) |  |
| is_import_children | bool |  |

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
| src_node | [Node](../../node/) |  |
| is_import_children | bool |  |
| import_format_mode | [ImportFormatMode](../../importformatmode/) |  |

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
src_doc = aw.Document()
dst_doc = aw.Document()

src_doc.first_section.body.first_paragraph.append_child(
    aw.Run(src_doc, "Source document first paragraph text."))
dst_doc.first_section.body.first_paragraph.append_child(
    aw.Run(dst_doc, "Destination document first paragraph text."))

# Every node has a parent document, which is the document that contains the node.
# Inserting a node into a document that the node does not belong to will throw an exception.
self.assertNotEqual(dst_doc, src_doc.first_section.document)
with self.assertRaises(Exception):
    dst_doc.append_child(src_doc.first_section)

# Use the "import_node" method to create a copy of a node, which will have the document
# that called the ImportNode method set as its new owner document.
imported_section = dst_doc.import_node(src_doc.first_section, True).as_section()

self.assertEqual(dst_doc, imported_section.document)

# We can now insert the node into the document.
dst_doc.append_child(imported_section)

self.assertEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dst_doc.to_string(aw.SaveFormat.TEXT))
```

Shows how to import node from source document to destination document with specific options.

```python
# Create two documents and add a character style to each document.
# Configure the styles to have the same name, but different text formatting.
src_doc = aw.Document()
src_style = src_doc.styles.add(aw.StyleType.CHARACTER, "My style")
src_style.font.name = "Courier New"
src_builder = aw.DocumentBuilder(src_doc)
src_builder.font.style = src_style
src_builder.writeln("Source document text.")

dst_doc = aw.Document()
dst_style = dst_doc.styles.add(aw.StyleType.CHARACTER, "My style")
dst_style.font.name = "Calibri"
dst_builder = aw.DocumentBuilder(dst_doc)
dst_builder.font.style = dst_style
dst_builder.writeln("Destination document text.")

# Import the Section from the destination document into the source document, causing a style name collision.
# If we use destination styles, then the imported source text with the same style name
# as destination text will adopt the destination style.
imported_section = dst_doc.import_node(src_doc.first_section, True, aw.ImportFormatMode.USE_DESTINATION_STYLES).as_section()
self.assertEqual(dst_style.font.name, imported_section.body.first_paragraph.runs[0].font.name)
self.assertEqual(dst_style.name, imported_section.body.first_paragraph.runs[0].font.style_name)

# If we use ImportFormatMode.KEEP_DIFFERENT_STYLES, the source style is preserved,
# and the naming clash resolves by adding a suffix.
dst_doc.import_node(src_doc.first_section, True, aw.ImportFormatMode.KEEP_DIFFERENT_STYLES)
self.assertEqual(dst_style.font.name, dst_doc.styles.get_by_name("My style").font.name)
self.assertEqual(src_style.font.name, dst_doc.styles.get_by_name("My style_0").font.name)
```

## See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [NodeImporter](../../nodeimporter/)
* enum [ImportFormatMode](../../importformatmode/)

