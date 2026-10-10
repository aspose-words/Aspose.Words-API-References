---
title: CompositeNode.append_child method
linktitle: append_child method
articleTitle: append_child method
second_title: Aspose.Words for Python
description: "CompositeNode.append_child method. Adds the specified node to the end of the list of child nodes for this node."
type: docs
weight: 80
url: /de/python-net/aspose.words/compositenode/append_child/
---

## append_child(new_child) {#node}

Adds the specified node to the end of the list of child nodes for this node.


```python
def append_child(self, new_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


### Examples

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
# Rufen Sie die \"RemoveAllChildren\"-Methode auf, um alle diese Knoten zu entfernen,
# und erhalten einen Dokumentknoten ohne Kinder.
doc.remove_all_children()
# Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
# Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
# Zuerst erstellen Sie einen neuen Abschnitt und fügen ihn dann als Kind zum Wurzel-Dokumentknoten hinzu.
section = aw.Section(doc)
doc.append_child(section)
# Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt
# auf der Seite zwischen dem Header und Footer des Abschnitts.
body = aw.Body(doc)
section.append_child(body)
# Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Schließlich fügen Sie etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
# setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

