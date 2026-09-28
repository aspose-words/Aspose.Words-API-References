---
title: SectionCollection indexer
linktitle: SectionCollection indexer
articleTitle: SectionCollection indexer
second_title: Aspose.Words for Python
description: "SectionCollection indexer. Retrieves a section at the given index."
type: docs
weight: 10
url: /de/python-net/aspose.words/sectioncollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a section at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows when to recalculate the page layout of the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Das Speichern eines Dokuments als PDF, als Bild oder das erstmalige Drucken wird automatisch
# den Layout des Dokuments innerhalb seiner Seiten zwischenspeichern.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Das Dokument auf irgendeine Weise ändern.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# In der aktuellen Version von Aspose.Words führt das Ändern des Dokuments nicht automatisch zu einem Neuaufbau
# des zwischengespeicherten Seitenlayouts. Wenn wir möchten, dass das zwischengespeicherte Layout
# auf dem neuesten Stand bleibt, müssen wir es manuell aktualisieren.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

Shows how to prepare a new section node for editing.

```python
doc = aw.Document()
# Ein leeres Dokument enthält einen Abschnitt, der einen Body hat, der wiederum einen Absatz enthält.
# Wir können Inhalte zu diesem Dokument hinzufügen, indem wir Elemente wie Text‑Runs, Formen oder Tabellen zu diesem Absatz hinzufügen.
self.assertEqual(aw.NodeType.SECTION, doc.get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.BODY, doc.sections[0].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[0].body.get_child(aw.NodeType.ANY, 0, True).node_type)
# Wenn wir einen neuen Abschnitt wie diesen hinzufügen, wird er keinen Body oder andere Kindknoten haben.
doc.sections.add(aw.Section(doc))
self.assertEqual(0, doc.sections[1].get_child_nodes(aw.NodeType.ANY, True).count)
# Führen Sie die Methode "EnsureMinimum" aus, um diesem Abschnitt einen Body und einen Absatz hinzuzufügen, um mit der Bearbeitung zu beginnen.
doc.last_section.ensure_minimum()
self.assertEqual(aw.NodeType.BODY, doc.sections[1].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[1].body.get_child(aw.NodeType.ANY, 0, True).node_type)
doc.sections[0].body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [SectionCollection](../)

