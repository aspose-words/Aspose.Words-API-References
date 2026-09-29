---
title: NodeImporter constructor
linktitle: NodeImporter constructor
articleTitle: NodeImporter constructor
second_title: Aspose.Words for Python
description: "aspose.words.NodeImporter constructor"
type: docs
weight: 10
url: /it/python-net/aspose.words/nodeimporter/__init__/
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
        # Scorri tutti i nodi a livello di blocco nel corpo della sezione,
        # quindi clona e inserisci ogni nodo che non è l'ultimo paragrafo vuoto di una sezione.
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
# Imposta la proprietà "KeepSourceNumbering" su "true" per applicare un ID di definizione elenco diverso
# agli stili identici con cui Aspose.Words li importa nei documenti di destinazione.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# Apri un documento con uno schema di numerazione elenco personalizzato, quindi clonalo.
# Poiché entrambi hanno lo stesso formato di numerazione, i formati entreranno in conflitto se importiamo un documento nell'altro.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# Quando importiamo il clone del documento nell'originale e poi lo aggiungiamo,
# allora le due liste con lo stesso formato elenco si uniranno.
# Se impostiamo il flag "KeepSourceNumbering" su "false", allora l'elenco dal clone del documento
# che aggiungiamo all'originale continuerà la numerazione dell'elenco a cui lo aggiungiamo.
# Questo unirà efficacemente le due liste in una sola.
# Se impostiamo il flag "KeepSourceNumbering" su "true", allora il clone del documento
# l'elenco manterrà la sua numerazione originale, facendo apparire i due elenchi come elenchi separati.
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

