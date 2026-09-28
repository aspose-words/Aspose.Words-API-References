---
title: Section.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Section.ensure_minimum method. Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/)."
type: docs
weight: 130
url: /de/python-net/aspose.words/section/ensure_minimum/
---

## ensure_minimum() {#default}

Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/).



```python
def ensure_minimum(self):
    ...
```

### Examples

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
* class [Section](../)

