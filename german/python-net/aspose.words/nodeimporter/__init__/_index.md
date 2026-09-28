---
title: NodeImporter constructor
linktitle: NodeImporter constructor
articleTitle: NodeImporter constructor
second_title: Aspose.Words for Python
description: "aspose.words.NodeImporter constructor"
type: docs
weight: 10
url: /de/python-net/aspose.words/nodeimporter/__init__/
---

## NodeImporter(src_doc, dst_doc, import_format_mode) {#documentbase_documentbase_importformatmode}

Initializes a new instance of the [NodeImporter](../) class.



```python
def __init__(self, src_doc: aspose.words.DocumentBase, dst_doc: aspose.words.DocumentBase, import_format_mode: aspose.words.ImportFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [DocumentBase](../../documentbase/) | The source document. |
| dst_doc | [DocumentBase](../../documentbase/) | The destination document that will be the owner of imported nodes. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

## NodeImporter(src_doc, dst_doc, import_format_mode, import_format_options) {#documentbase_documentbase_importformatmode_importformatoptions}

Initializes a new instance of the [NodeImporter](../) class.



```python
def __init__(self, src_doc: aspose.words.DocumentBase, dst_doc: aspose.words.DocumentBase, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [DocumentBase](../../documentbase/) | The source document. |
| dst_doc | [DocumentBase](../../documentbase/) | The destination document that will be the owner of imported nodes. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) | Specifies various options to format imported node. |

## Examples

Shows how to insert the contents of one document to a bookmark in another document (InsertDocument).

```python
@staticmethod
def insert_document(insertion_destination, doc_to_insert):
    if insertion_destination.node_type == aw.NodeType.PARAGRAPH or insertion_destination.node_type == aw.NodeType.TABLE:
        destination_parent = insertion_destination.parent_node
        importer = aw.NodeImporter(src_doc=doc_to_insert, dst_doc=insertion_destination.document, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
        # Durchlaufen Sie alle Block‑Ebene‑Knoten im Body des Abschnitts,
        # dann klonen und einfügen Sie jeden Knoten, der nicht der letzte leere Absatz eines Abschnitts ist.
        for src_section in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_section(), b), list(doc_to_insert.sections))):
            for src_node in src_section.body:
                if src_node.node_type == aw.NodeType.PARAGRAPH:
                    para = src_node.as_paragraph()
                    if para.is_end_of_section and (not para.has_child_nodes):
                        continue
                new_node = importer.import_node(src_node, True)
                destination_parent.insert_after(new_node, insertion_destination)
                insertion_destination = new_node
    else:
        raise Exception()
```

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - destination.docx')
# Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true", um eine andere Listendefinitions‑ID anzuwenden
# auf identische Stile, wie Aspose.Words sie in Zieldokumente importiert.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# Öffnen Sie ein Dokument mit einem benutzerdefinierten Listennummerierungsschema und klonen Sie es dann.
# Da beide das gleiche Nummerierungsformat haben, werden die Formate kollidieren, wenn wir ein Dokument in das andere importieren.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# Wenn wir die Kopie des Dokuments in das Original importieren und dann anhängen,
# werden die beiden Listen mit dem gleichen Listenformat zusammengeführt.
# Wenn wir das Flag "KeepSourceNumbering" auf "false" setzen, dann wird die Liste aus der Dokumentkopie
# die wir an das Original anhängen, die Nummerierung der Liste übernehmen, an die wir sie anhängen.
# Damit werden die beiden Listen effektiv zu einer zusammengeführt.
# Wenn wir das Flag "KeepSourceNumbering" auf "true" setzen, dann wird die Dokumentkopie
# Die Liste behält ihre ursprüngliche Nummerierung bei, sodass die beiden Listen als separate Listen erscheinen.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = keep_source_numbering
importer = aw.NodeImporter(src_doc=src_doc, dst_doc=dst_doc, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options=import_format_options)
for paragraph in src_doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    imported_node = importer.import_node(paragraph, True)
    dst_doc.first_section.body.append_child(imported_node)
dst_doc.update_list_labels()
if keep_source_numbering:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
else:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '10. Item 1\r\n' + '11. Item 2 \r\n' + '12. Item 3\r\n' + '13. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
```

## See Also

* module [aspose.words](../../)
* class [NodeImporter](../)

