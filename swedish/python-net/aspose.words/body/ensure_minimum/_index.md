---
title: Body.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Body.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 70
url: /sv/python-net/aspose.words/body/ensure_minimum/
---

## ensure_minimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Clears main text from all sections from the document leaving the sections themselves.

```python
doc = aw.Document()
# Ett tomt dokument innehåller en sektion, en kropp och ett stycke.
# Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
# och sluta med ett dokumentnod utan några barn.
doc.remove_all_children()
# Detta dokument har nu inga sammansatta barnnoder som vi kan lägga till innehåll i.
# Om vi vill redigera det måste vi återfylla dess nodsamling.
# Först, skapa en ny sektion och lägg sedan till den som ett barn till rot-dokumentnoden.
section = aw.Section(doc)
doc.append_child(section)
# En sektion behöver en kropp, som kommer att innehålla och visa allt dess innehåll
# på sidan mellan sektionens sidhuvud och sidfot.
body = aw.Body(doc)
section.append_child(body)
# Denna kropp har inga barn, så vi kan ännu inte lägga till runs i den.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# Anropa "EnsureMinimum" för att säkerställa att denna kropp innehåller minst ett tomt stycke.
body.ensure_minimum()
# Nu kan vi lägga till runs i kroppen och få dokumentet att visa dem.
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Body](../)

