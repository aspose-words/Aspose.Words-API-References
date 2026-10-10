---
title: CompositeNode.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "CompositeNode.count property. Gets the number of immediate children of this node."
type: docs
weight: 10
url: /sv/python-net/aspose.words/compositenode/count/
---

## CompositeNode.count property

Gets the number of immediate children of this node.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# Ett tomt dokument har som standard ett stycke.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Sammansatta noder, såsom vårt stycke, kan innehålla andra sammansatta och inline-noder som barn.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# Skapa tre ytterligare körnoder.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# Dokumentkroppen kommer inte att visa dessa körningar förrän vi infogar dem i en sammansatt nod
# som i sig är en del av dokumentets nodträd, som vi gjorde med den första körningen.
# Vi kan bestämma var textinnehållet i noder som vi infogar
# visas i dokumentet genom att ange en infogningsplats relativt en annan nod i stycket.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# Infoga den andra körningen i stycket framför den ursprungliga körningen.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# Infoga den tredje körningen efter den ursprungliga körningen.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# Infoga den första körningen i början av styckets samling av barnnoder.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# Vi kan ändra innehållet i körningen genom att redigera och ta bort befintliga barnnoder.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

