---
title: Section.body property
linktitle: body property
articleTitle: body property
second_title: Aspose.Words for Python
description: "Section.body property. Returns the [Body](../../body/) child node of the section."
type: docs
weight: 20
url: /de/python-net/aspose.words/section/body/
---

## Section.body property

Returns the [Body](../../body/) child node of the section.



```python
@property
def body(self) -> aspose.words.Body:
    ...

```

### Remarks

[Body](../../body/) contains main text of the section.

Returns ``None`` if the section does not have a [Body](../../body/) node among its children.




### Examples

Clears main text from all sections from the document leaving the sections themselves.

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
# Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt
# auf der Seite zwischen dem Header und Footer des Abschnitts.
body = aw.Body(doc)
section.append_child(body)
# Dieser Body hat keine Kinder, daher können wir noch keine Runs hinzufügen.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# Rufen Sie "EnsureMinimum" auf, um sicherzustellen, dass dieser Body mindestens einen leeren Absatz enthält.
body.ensure_minimum()
# Jetzt können wir Runs zum Body hinzufügen und das Dokument dazu bringen, sie anzuzeigen.
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

