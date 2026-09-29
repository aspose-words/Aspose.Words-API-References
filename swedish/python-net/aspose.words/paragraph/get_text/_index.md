---
title: Paragraph.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "Paragraph.get_text method. Gets the text of this paragraph including the end of paragraph character."
type: docs
weight: 280
url: /sv/python-net/aspose.words/paragraph/get_text/
---

## get_text() {#default}

Gets the text of this paragraph including the end of paragraph character.


```python
def get_text(self):
    ...
```

### Remarks

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:


* If the paragraph is the last paragraph of [Body](../../body/), then
  [ControlChar.SECTION_BREAK](../../controlchar/SECTION_BREAK/) (\\x000c) is appended.
  
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then
  [ControlChar.CELL](../../controlchar/CELL/) (\\x0007) is appended.
  
* For all other paragraphs
  [ControlChar.PARAGRAPH_BREAK](../../controlchar/PARAGRAPH_BREAK/) (\\r) is appended.
  
The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




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
* class [Paragraph](../)

